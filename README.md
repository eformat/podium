# Podium
Communication is the key to any high performing team. Podium is a containerized deployment of a set of leading opensource communication tools that allow teams interact more effectively in a remote (post COVID-19) world. Podium brings tools together in a way that that allows not only a team to interact better but even more inportantly allows non-team members to interact effectively. Podium current provides the following components:
* [Dashboard (Mozaik)](http://mozaik.rocks/)
* [Chat (Mattermost)](https://mattermost.com/)
* [Video Conferencing (Jitsi Meet)](https://jitsi.org/jitsi-meet/)
* [Real-time Document Editing (Etherpad)](https://etherpad.org/)

An instance of podium will deploy all components and configure a dashboard so all team and non-team members can interact immediately as well as effectively.

## Feature requests
If you would like to see a feature or addition please open a issue and feel welcome to contribute.

## Lets Encrypt Certificate
Jitsi meet requires a TLS certificate. TLS can be terminated inside the web pod or terminated on the edge. I would recommend edge termination and in this case we can use a lets encrypt k8s admission controller to setup our certificates within the created OpenShift route.

[Setup Lets Encrypt on OpenShift](https://keithtenzer.com/2020/04/03/openshift-application-certificate-management-with-lets-encrypt/)

## Deployment
You can deploy Podium using [Podium Operator](docs/OPERATOR.DEPLOYMENT.md) for OpenShift 4 or [Deployment Templates](docs/TEMPLATE_DEPLOYMENT.md) for OpenShift 3/4.
