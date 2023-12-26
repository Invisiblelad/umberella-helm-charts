## This is an umberella chart which is used to deploy a lot of application in one go ##

 # Here we are deploying the redis and postgres along with nginx

Step:1

 You have to add the required dependencies in the chart .yaml like redis and postgres.

Step:2
  
 Then update download the helm chart by using below command.It will pull the respective charts from mentioned repositories.
  
  `helm dependency update`

Step:3
  The downloaded charts can be seen in the charts folder

Step:4
  If you want to overwrite any of the charts values from parent nginx chart.Then go to parent values.yaml and add the respective subchart and it'ss values that need to be overidden.Refer value.yaml to see the changes.

Step:
  Deploy the chart with below command .It will deploy all the respective dependency charts

  `helm install `<name>` umberella-chart -n `<namespace>``
