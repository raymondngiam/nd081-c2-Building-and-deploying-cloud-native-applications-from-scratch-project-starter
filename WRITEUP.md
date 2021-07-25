### Serverless Functions

1. A MongoDB database in Azure CosmosDB service is created and initialized with the sample data provided.

    <img src='solution_images/mongodb1-advertisements.png'>

    <img src='solution_images/mongodb2-posts.png'>

2. The finished server-side application contains working Azure Functions for HTTP Triggers in Python.

    <img src='solution_images/functionapp-url.png'>
    <img src='solution_images/functionapp-endpoints.png'>

3. The Azure Functions HTTP Trigger endpoints can connect to MongoDB in Azure CosmosDB service.

    <img src='solution_images/functionapp-getAdvertisements.png'>

4. The client-side application in Flask should be able to call the live Functions API endpoints that the students published in previous steps.

    <img src='solution_images/client-side2.png'>

    <img src='solution_images/client-side0.png'>


### Logic Apps and Event Hubs

1. The student demonstrates mastery in using Azure Logic App Designer to create a trigger.

    <img src='solution_images/logicapp-sendgrid1.png'>

    <img src='solution_images/logicapp-sendgrid2.png'>

2. The student should be able to create a custom event grid topic and publish the topic.


    <img src='solution_images/eventhubtrigger1.png'>

3. The student should be able to add the connection string of the event hub to the Azure Function.

    - Create and copy `Shared Access Policy` connection string

        <img src='solution_images/eventhubtrigger2.png'>

    - Add `EventHubConnectionString` into function app appsetting

        <img src='solution_images/eventhubtrigger3.png'>

    - In `eventHubTrigger`'s `function.json` setting

        ```json
        {
        "scriptFile": "__init__.py",
        "bindings": [
            {
            "type": "eventHubTrigger",
            "name": "event",
            "direction": "in",
            "eventHubName": "hub1", 
            "connection": "EventHubConnectionString"
            }
        ]
        }
        ```

### Deploying Your Application

1. The student should be able to deploy their Neighborly web application on Azure App Service.

    <img src='solution_images/client-side1.png'>

    <img src='solution_images/client-side3.png'>

2. The student should be able to containerize their Flask application with Dockerfile.

    <img src='solution_images/dockerfileACR.png'>

3. The code demonstrates an automated pipeline to spin Kubernetes services in Azure.

    <img src='solution_images/aks-deploy1.png'>

    <img src='solution_images/aks-deploy2.png'>