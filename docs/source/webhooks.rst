########
Webhooks
########


When a form is posted from a webhook the format will be as follows:

.. code-block:: javascript

    {
      "id": "__form_hash_id__",
      "__field_hash_id__": "Field Data",
      "files": {
        "__field_hash_id__": "S3 Bucket Link"
      }
    }

You can get your form hash_id and the layout of the entire form from the following links:

For a list of forms, the endpoint is:
https://(your_subdomain).blitzen.com/api/v1/forms/

If you want information about a forms fields, like labels and other configuration, the endpoint is:
https://(your_subdomain).blitzen.com/api/v1/forms/__form_hash_id__/fields/

You can post the webhook in 2 different formats, which are ``applicaiton/json`` and ``application/x-www-form-encoded``

``application/json`` will post the data within the body of the request

``application/x-www-form-encoded`` will append all the data to the url
