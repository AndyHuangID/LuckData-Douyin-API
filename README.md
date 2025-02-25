# LuckData-Douyin-API

Luckdata provides an API with 100 free credits every month. This allows small businesses or individuals with low data requirements to use the API for tasks such as testing and data analysis.

The LuckData Douyin API is a powerful data interface designed for developers and businesses to efficiently scrape trending rankings, video details, challenge leaderboards, and more from Douyin. With this API, you can easily access real-time data and analyze content trends to optimize your social media strategies.

# How to Use
Step 1: Click “Get Started”
Step 2: Purchase a plan and complete the payment
Step 3: Choose your preferred run mode
Step 4: Click "Test Endpoint"

# Code Snippets

## python

<pre>import requests

headers = {
    'X-Luckdata-Api-Key': 'your key'
}

json_data={}

response = requests.get(
    'https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223',
    headers=headers,
    
)
print(response.json())</pre>

## Java

<pre>import java.io.IOException;
import java.net.URI;
import java.net.http.HttpClient;
import java.net.http.HttpRequest;
import java.net.http.HttpResponse;

HttpClient client = HttpClient.newHttpClient();

HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223"))
    .GET()
    
    .setHeader("X-Luckdata-Api-Key", "your key")
    .build();

HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());</pre>

## go

<pre>package main

import (
  "fmt"
  "io"
  "log"
  "net/http"
  "strings"
)

func main() {
  client := &http.Client{}
  var data = nil
  req, err := http.NewRequest("GET", "https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223", data)
  if err != nil {
    log.Fatal(err)
  }
  
  req.Header.Set("X-Luckdata-Api-Key", "your key")
  resp, err := client.Do(req)
  if err != nil {
    log.Fatal(err)
  }
  defer resp.Body.Close()
  bodyText, err := io.ReadAll(resp.Body)
  if err != nil {
    log.Fatal(err)
  }
  fmt.Printf("%s\n", bodyText)
}</pre>

## shell

<pre>curl -X GET "https://luckdata.io/api/douyin-API/get_xv5p?city=110000&type=rise_heat&end_date=20241224&page_size=10&start_date=20241223"  -H "X-Luckdata-Api-Key":"your key" </pre>

# more
more about douyin api please click: <a href="https://luckdata.io/marketplace/detail/douyin-API">LuckData Douyin API</a>
