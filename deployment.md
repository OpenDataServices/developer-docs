# Deployment

## General approach

We do nearly all of our deployment with the salt deployment tool. http://saltstack.com/

The repository at https://github.com/OpenDataServices/opendataservices-deploy provides lots of information for those familiar with salt.

We currently take a middle ground approach for semi automated deployments for our small setup. This has been described as "Pets with strong configuration management", in slide 17 from these [slides from CERN](http://www.slideshare.net/gmccance/cern-data-centre-evolution):

Future application architectures should use Cattle, but pets with strong configuration management are viable and still needed.

