# URL Shorterner

<div>
    <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white">
    <img src="https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white">
    <img src="https://img.shields.io/badge/Amazon%20S3-FF9900?style=for-the-badge&logo=amazons3&logoColor=white">
    <img src="https://img.shields.io/badge/IntelliJ_IDEA-000000.svg?style=for-the-badge&logo=intellij-idea&logoColor=white">
</div>
<br>

This project was developed as part of the **_Curso Gratuito de Java_** by **Rocketseat**. The goal was to build a 
**Serverless URL shortener** using **Java**, **AWS Lambda**, and **API Gateway**.

The application features two **endpoints** managed by **API Gateway**, which communicate with **Lambda functions** to **store** and **retrieve URLs** from an **S3 bucket**.

- **POST Endpoint**:  
  Users submit a **URL** and an **expiration time**, receiving a unique **code** in return.

- **GET Endpoint**:  
  The user can use the provided **code** to retrieve and **render** the saved **URL**.

## Technologies

- Java 21
- AWS Lambda
- S3 Bucket
- API Gateway

## Testing

To test the application, you can use **Postman**, **Insomnia**, or any similar software. Follow the instructions below, and you should encounter no issues.

**Note**: AWS Lambda has a **"cold start"**, so it may take a few seconds to return a response.

---

1. Make a **POST** request with a JSON object in the following structure to this URL: 
``https://c3ix2qd8t5.execute-api.sa-east-1.amazonaws.com/create``<br><br>
   - ``originalUrl``: The URL you want to shorten.
   - ``expirationTime``: The time when the link should expire, in Epoch format.
    ```json
    {
        "originalUrl": "https://example.com",
        "expirationTime": "1672531200"
    }
    ```
   
   **TIP:** Use [Epoch Converter](https://www.epochconverter.com/) to generate the expiration time.<br><br>

2. You should receive a response like this:
    ```json
    {
        "code": "799021a4"
    }
    ```
   <br>

3. Copy the **code** from the response, append it to the following URL and make a **GET** request: 
``https://c3ix2qd8t5.execute-api.sa-east-1.amazonaws.com/``<br><br>
    Example:
    ```
    https://c3ix2qd8t5.execute-api.sa-east-1.amazonaws.com/799021a4
    ```
   ***Note:*** You can access the URL with the code in a browser like Chrome, Opera, or any similar tool, and it will 
redirect you to the saved page.

## GitHub
[![Top Langs](https://github-readme-stats-git-masterrstaa-rickstaa.vercel.app/api/top-langs/?username=sergiotavuencas)](https://github.com/anuraghazra/github-readme-stats)
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=sergiotavuencas\&hide=issues\&show_icons=true)

## Contact
Feel free to reach out to me through my social media if you have questions about my career, projects I’m working on, what I’m studying, or any advice you might have, whether career-related or suggestions for improvements in my code.

<div>
  <a href="http://www.linkedin.com/in/sergiotavuencas" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a>
  <a href="https://github.com/sergiotavuencas/" target="_blank"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" target="_blank"></a>
  <a href="mailto:sergio_tavuencas@outlook.com"><img src="https://img.shields.io/badge/Microsoft_Outlook-0078D4?style=for-the-badge&logo=microsoft-outlook&logoColor=white" target="_blank"></a>
  <a href="mailto:sergiovicentetavuencas@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
</div>
