# 1. Firstname, Lastname, Github ID and Email address of the 3 members of the homework group. Link to the Github repositories of your homework.

* Junior N'nane (https://gihub.com/nprime496) / Mail  : dieudonne-junior.n-nane@grenoble-inp.org
* Cheikh Saliou Diagne (https://gihub.com/diagnecs) / Mail : cheikh-saliou.diagne@grenoble-inp.org

Repo of Homework:

https://github.com/nprime496/mastering-microservices


# 2. Deployment of Microservices with JHipster on GCP (screenshot of your GCP console)

Generation and deploymen of services was done following following the tutorial `mastering-microservices/microservices/microservices.md`

![](./media/gateway-deploy.png)
![](./media/services-up.png)

Services were deployed using Kubernetes cluster on Google Cloud Platform.

![](./media/cluster.png)

Services were successfully deployed:

![](./media/services.png)

![](./media/app-cloud.png)


## (bonus) pushing to gcloud registry 

We also tested pushing container images to Google Cloud Container Registry.

```
docker tag productorder gcr.io/$PROJECTID/productorder
docker push gcr.io/$PROJECTID/productorder
```

![](./media/registry-container.png)


# 3. Enabling scalability on GCP for one microservice (screenshot of your GCP console)

[Scaling an application](https://cloud.google.com/kubernetes-engine/docs/how-to/scaling-apps)


we choose to scale `invoice` app.

`kubectl scale deployments -n store invoice --replicas 4`

![](./media/scale-up.png)

We can see that it the number of possible instance was upgraded on GCP as well:

![](./media/scale-up-cloud.png)

# 4. Monitoring dashboard (screenshot of prometheus+grafana dashboard OR screenshot of your GPC dashboard)

We monitored application using Prometheus:

![](./media/monitor1.png)

![](./media/monitor2.png)

![](./media/monitor3.png)


And checked health using GCP:

![](./media/gcp.png)

# 5. Load injection with Gatling for demonstrating scalability (screenshot of grafana OR screenshot of your GPC dashboard + link to your gatling report)


![](./media/gatling-experiment.png)
![](./media/report1.png)
![](./media/report2.png)
![](./media/report3.png)

Reports generated are available in [result folder](./gatling-charts-highcharts-bundle-2.3.1/results/)


