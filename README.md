## Unfurl for Campsite

This repository contains an Unfurl project for deploying a demonstration version of [Campsite](https://github.com/dnielsen/campsite) to a compute instance on AWS and Google Cloud.

Unfurl runs on any Linux or Mac machine with Python (3.7 or later) and Git installed. To install it run:

`pip install unfurl`

Now you can clone ensembles just like you would clone a git repository.
To clone it, run:

``unfurl clone https://github.com/onecommons/unfurl_campsite.git``


To deploy your app of AWS or GCP:

``cd unfurl_campsite`` 

and then either

``unfurl deploy aws``

or 

``unfurl deploy gcp``

For unfurl to have access to your cloud provider account you will need to have setup default credentials or you can set their environment variables (e.g. AWS_ACCESS_KEY_ID or GOOGLE_APPLICATION_CREDENTIALS).

If you just installed `unfurl` this will take a few minutes as it creates your
`unfurl_home` and installs its dependencies. Then it will deploy the ensemble and the final lines of output should look like:

```
  > Outputs:
  >  site_url: http://127.0.0.1:4000/
```

To destroy the instance you have created, run:

``unfurl undeploy aws`` or ``unfurl undeploy gcp``
