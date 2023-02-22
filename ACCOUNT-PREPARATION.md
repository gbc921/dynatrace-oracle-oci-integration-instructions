> **Warning**
>
> This project is under development. 


# Take note of needed information

1. Click on the user icon in the top-right and then "Tenancy"
    * Take note of the "OCID": it will be something like `ocid1.tenancy.oc1..<unique_ID>`
    * Take note of the "Object storage namespace": it will be a 12-character unique id (this will be called "tenancy namespace")

# Create an application

1. Access Developer Services > Applications
1. Create application with name "dynatrace-integration"
1. Access the application created
1. Go to Configuration
1. Add the following environment variables 
    * `enable_log_forwarding`: 'true' or 'false'
    * `enable_metric_forwarding`: 'true' or 'false'
    * `dynatrace_token`: 
        * Permission for log forwarding: API v2 "Ingest logs"
        * Permission for metric forwarding: API v2 "Ingest metrics"
    * `dynatrace_environment`: the url of the environment

# Create a resource in a service to generate logs and metrics

You can use any of the supported services, this is just an example.

1. Access Storage > Buckets
1. Create Bucket with default options

* [Supported service for metrics](https://docs.oracle.com/en-us/iaas/Content/Monitoring/Concepts/monitoringoverview.htm#SupportedServices)
* [Supported services for logs](https://docs.oracle.com/en-us/iaas/Content/Logging/Concepts/service_logs.htm)
