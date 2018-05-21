# Unit Testing


### Assertions for APIs

#### Python examples

##### assert outputs
Here, we assert that the response data from the output
function is the same output as the one that we expect.
```python

def output(response_type, message, download_link):
    if download_link == ‘’:
       response = [
        {
             ‘type’: response_type,
             ‘message’: message
         }
     ]
     else:
     response = [
      {
              ‘type’: response_type,
              ‘message’: message,
              ‘download_link’: download_link
       }
     ]
     return jsonify({‘response’: response})

def test_output(self):
    with app.test_request_context():
        # mock object
        out = output(‘error’, ‘Test Error’, ‘local_host’)
        # Passing the mock object
        response = [
          {
                 ‘type’: ‘error’,
                 ‘message’: ‘Test Error’,
                 ‘download_link’: ‘local_host’
           }
        ]
        data = json.loads(out.get_data(as_text=True)
        # Assert response
        self.assertEqual(data[‘response’], response)
```

###### assert 200



# Sources

https://www.grossum.com/blog/beginner-s-guide-to-automating-api-tests-using-python


https://hackernoon.com/writing-unit-tests-for-rest-api-in-python-web-application-2e675a601a53


https://docs.microsoft.com/en-us/aspnet/core/testing/integration-testing?view=aspnetcore-2.0
