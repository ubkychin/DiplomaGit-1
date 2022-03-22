# Accessing the Underlying MongoDb with C# using Resharpr

## GET all documents from the products collection
    var client = new RestClient("https://diplomagit-e6cc.restdb.io/rest/products");
    var request = new RestRequest(Method.GET);
    request.AddHeader("cache-control", "no-cache");
    request.AddHeader("x-apikey", "35ef07b4da07e33f8da131df3ef7b29b87d9e");
    request.AddHeader("content-type", "application/json");
    IRestResponse response = client.Execute(request);

## POST a new document to the products collection --
    var client = new RestClient("https://diplomagit-e6cc.restdb.io/rest/products");
    var request = new RestRequest(Method.POST);
    request.AddHeader("cache-control", "no-cache");
    request.AddHeader("x-apikey", "35ef07b4da07e33f8da131df3ef7b29b87d9e");
    request.AddHeader("content-type", "application/json");
    request.AddParameter("application/json", "{\"field1\":\"xyz\",\"field2\":\"abc\"}", ParameterType.RequestBody);
    IRestResponse response = client.Execute(request);

## PUT an updated document to the products collection --
    var client = new RestClient("https://diplomagit-e6cc.restdb.io/rest/products/(ObjectID)");
    var request = new RestRequest(Method.PUT);
    request.AddHeader("cache-control", "no-cache");
    request.AddHeader("x-apikey", "35ef07b4da07e33f8da131df3ef7b29b87d9e");
    request.AddHeader("content-type", "application/json");
    request.AddParameter("application/json", "{\"field2\":\"new value\"}", ParameterType.RequestBody);
    IRestResponse response = client.Execute(request);

## DELETE a document from the products collection
    var client = new RestClient("https://diplomagit-e6cc.restdb.io/rest/products/(ObjectID)");
    var request = new RestRequest(Method.DELETE);
    request.AddHeader("cache-control", "no-cache");
    request.AddHeader("x-apikey", "35ef07b4da07e33f8da131df3ef7b29b87d9e");
    request.AddHeader("content-type", "application/json");
    IRestResponse response = client.Execute(request);