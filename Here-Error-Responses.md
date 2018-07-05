# Here Error Responses #

## Introduction ##

While working with one of the HERE API or SDK packages, you may receive error responses from the HERE Server. The following sections describe the error structures, codes and messages you may receive.

<a name="GRPCErrorStructure"></a>
## GRPC Error Structures ##

In error situations, all endpoints return a GRPC Status object as defined below.

    type Status struct {
        // The error code (a value from the google.rpc.Code enum)
        Code int32
        // A textual, informative, English-language error message
        Message string
        // A list of messages describing the error details
        Details []*google_protobuf.Any
    }

>**NOTE**: If the GRPC-gateway fails to identify the server error, it creates a new GRPC error with an UNKNOWN error code (which is mapped to the HTTP 500 Internal Server Error).

The **Details** field of the **Status** structure contains the following nested structure:

    type ExternalError struct {
       // The external error code
       Code int32 `protobuf:"varint,1,opt,name=code" json:"code,omitempty"`
       // Locale code (see http://www.rfc-editor.org/rfc/bcp/bcp47.txt)
       // Note: currently the only supported Locale is "en-US". 
       Locale string `protobuf:"bytes,1,opt,name=locale" json:"locale,omitempty"`
       // The error message, localized by locale.
       // The Message string is the same as the message string in the Status structure.
       Message string `protobuf:"bytes,2,opt,name=message" json:"message,omitempty"`
    }

## RESTful JSON Error Structure ##

The GRPC error is translated to its RESTful JSON representation automatically by the GRPC-gateway package. The JSON body contains the error code, locale and message values from the Status structure shown above.

Here is an example of a JSON-formatted error:

    Header Code: 404
    Body:
    {
        "code": 40400,
        "locale: "en-US"
        "message": "Requested item not found"
    }
 
The GRPC error code is translated to an HTTP header status code, according to the mapping in the following table:

GRPC Error Code	| HTTP Error Code
:---------------|:----------------
InvalidArgument	|StatusBadRequest (400)
OutOfRange	|StatusBadRequest (400)
PermissionDenied	|StatusForbidden (403)
Unauthenticated	|StatusUnauthorized (401)
NotFound	|StatusNotFound (404)
AlreadyExists	|StatusConflict (409)
FailedPrecondition	|StatusPreconditionFailed (412)
Internal	|StatusInternalServerError (500)
Unimplemented	|StatusNotImplemented (501)
Unknown	|StatusInternalServerError (500)
 
## Error Categories ##

All external errors have one of the categories described in the following table:

Error Category	| Description
:---------------|:------------
**Input**	|	Error in request input.<br/><br/>Possible GRPC codes:<br/><br/>InvalidArgument(3) – missing, malformed or otherwise invalid argument<br/><br/>OutOfRange(11) – value has the correct type but is out of the valid range
**Permissions**|Authorization or authentication error.<br/><br/>Possible GRPC codes:<br/><br/>**PermissionDenied(7)** – attempt to perform an action for which the user has no permissions<br/><br/>**Unauthenticated(16)** – the user failed to be authenticated
**Communication** | Connection error or timeout when accessing other services.<br/><br/>Possible GRPC codes:<br/><br/>**Unavailable(14)** – the service is unavailable
**Business Logic** | The request or its data is incompatible with the current server state.<br/><br/>Possible GRPC codes:<br/><br/>**NotFound(5)** – requested item was not found (for example, a ride ID)<br/><br/>**AlreadyExists(6)** – attempt to create an entity that already exists<br/><br/>**FailedPrecondition(9)** – the request does not meet a required condition (for example, a delete was requested when delete is not allowed)<br/><br/>**Internal(13)** – other error in business logic
**Other** 	|	Miscellaneous errors.<br/><br/>Possible GRPC codes:<br/><br/>**Internal(13)** – error in business logic<br/><br/>**Unimplemented(12)** - the endpoint is not implemented yet.

## Error Codes ##

The following table describes the error codes that Here API clients can receive:

Domain|	Error|	Code
:-----|:-----|:------
Request	| Invalid request |	40000
Request	|Requested item not found|	40400
Request	|Request timeout|	40800
Request	|Failed Dependency	|42400
Connection	|Too many requests|	42900
--	|Internal server error|	50000
--	|Not Implemented|	50100
Authorization	|Permission denied	|40300
Authentication	|Invalid token|	40101
Authentication	|Token expired	|40102

## References ##

[https://cloud.google.com/apis/design/errors](https://cloud.google.com/apis/design/errors)

[https://github.com/grpc/grpc-go/tree/master/examples/rpc_errors](https://github.com/grpc/grpc-go/tree/master/examples/rpc_errors)

[https://jbrandhorst.com/post/grpc-errors](https://jbrandhorst.com/post/grpc-errors)
