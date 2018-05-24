## Propose New Resource API

This API allows users to submit a new resource order request to CORAL Resource module via a client form. 

### The API and the Client Form 
The API is based on [Flight](http://flightphp.com/), a simple and extensible framework for PHP.   

![Screenshot of API Client Form](img/api/apiClientForm.PNG)

This is a sample of a client form, which is based on [unirest]( http://unirest.io/php.html ). Users can enter resource information in the form. This includes basic information about the resource including Title, Description, Provider, ISBN/ISSN, URL and information about the order such as fund code and cost. For Format, Acquisition Type, Resource Type, and Fund code, the data showing on the form are populated from the data predefined in Coral Admin tab. Data entered here are mapped to fields in CORAL Resources. Other fields without a matching CORAL field are loaded into CORAL as general notes. If a specific note type is created in CORAL, they can be mapped to the desired note type.  

Once submitted, a report is presented with a summary of the fields. A new resource record is created automatically in CORAL Resource module. If data entered in Format, Acquisition Type and Resource Type match with what determine a workflow, the workflow is triggered once the record is submitted via the client form. 

### API Configuration

#### Server-side:

Edit resources/admin/configuration.ini and fill apiAuthorizedIP with the IP address of the client accessing the API:
apiAuthorizedIP="192.168.1.1"

You can set multiple IPs (comma-separated):
apiAuthorizedIP="192.168.1.1,192.168.2"

You can also set incomplete IPs so the whole range will be allowed:
apiAuthorizedIP="192.168.1"
(will authorize all IPs from 192.168.1.1 to 192.168.1.255)

If you are trying to test the example form and it is on the same machine as Coral, 127.0.0.1 should work.

Hint: if you don't know which IP address will be requesting the API, just leave apiAuthorizedIP blank (apiAuthorizedIP="") and access the example form with your browser (http://yourcoral.tld/resources/api_client/ ), you will get an error like this:
You are not authorized to use this service.
Unauthorized IP: 127.0.0.1

#### Client-side:

Edit api_client/index.php and set the $server variable:
$server = "http://yourcoral.tld/resources/api/"; 

Note that the Acquisition Type is hardcoded to show two options Approved and Need Approval. This can be customized to show desired acquisition types by modifying index.php (in the api_client folder). Users can either edit line 330 or remove line 330 and line 334. See the code in the screenshot below. 

![Screenshot of API Client IndexPHP File](img/api/apiClientIndexphp.PNG)
