# Como desenvolver aplicações em Java para Amazon Web Services 
Esse repositório de código fonte é relacionado a esse [livro](http://leanpub.com/amazonwebservice), sobre como desenvolver aplicações em **Java**  utilizando **Spring Boot** para serem executadas na **Amazon Web Services**, utilizando *container* **Docker** e [AWS ECS](https://aws.amazon.com/ecs/). 

Nesse exemplo será construída uma aplicação com serviços REST para cadastro de produtos de uma loja. Tais produtos serão armazenados em um banco de dados MySQL utilizando o [AWS RDS](https://aws.amazon.com/rds/). Em cada operação de cadastro, exclusão ou alteração de um produto, um evento será publicado em um tópico do [AWS SNS](https://aws.amazon.com/sns), permitindo a integração com outras aplicações. Essa aplicação também fará importação de arquivos de notas fiscais através do [AWS S3](https://aws.amazon.com/s3/).

Veja a seguir um diagrama com os serviços da AWS que são utilizados.

![Diagrama da aplicação e serviços AWS utilizados](images/167_sns_chapter_02.png)

Para aprender esses e outros conceitos sobre desenvolvimento de aplicações utilizando Amazon Web Services, não deixe de conferir esse [livro](http://leanpub.com/amazonwebservice)!

Confira também os outros repositórios de código relativos a esse livro:

- [Project02](https://github.com/siecola/aws_project02): esse projeto contará com uma tabela do [AWS DynamoDB](https://aws.amazon.com/dynamodb), para armazenar os eventos gerados pela aplicação de cadastro de produtos, integrado através de uma fila do [AWS SQS](https://aws.amazon.com/sqs/).
- [Lambda01](https://github.com/siecola/aws_lambda01): esse será um exemplo simples de uma aplicação *serverless* utilizando funções com o [AWS Lambda](https://aws.amazon.com/lambda/), demonstrando como agendar a execução de uma função.
- [Lambda02](https://github.com/siecola/aws_lambda02): nesse segundo exemplo, será demonstrado como executar uma função **Lambda** através de um evento publicado no **SNS**.
- [Lambda03](https://github.com/siecola/aws_lambda03): aqui será apresentado como criar uma função **Lambda** para consumir arquivos importados no **S3** e gravar seus dados em uma tabela do **DynamoDB**.