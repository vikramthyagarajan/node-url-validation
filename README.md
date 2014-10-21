node-url-validation
===================

Provides simple URL validation in a restify/express/connect application. There are 3 types of validation, and each works differently-

  - Query Validation
    Here, there are a set of allowed fields and subfields. When stuff is set otherwise, a validation error is sent out. Also, if no fields are set, then a default value is set. This is for url which can provide data depending on what fields are required by the user. Mostly, just GET calls.
    Other Validations like for pagination also come under this. Access tokens and other authorization tasks are not taken care of by this module.

  - Body Validation
    This is to check the body of the request sent. Mostly to be used in POST and PUT calls to make sure that the client is sending correct Data. Here, the allowed fields are set, and the required fields. The type of each field can either be explicitly specified, or a mongoose schema can be given, and validation occurs automatically based on the schema.

  - Params Validation
    This is to check the URL of the request. Incase there are parameters, then validation can be done against those parameters.

