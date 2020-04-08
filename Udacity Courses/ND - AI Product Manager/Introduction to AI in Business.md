# Introduction to AI in Business

## Lesson 1 - Welcome

The ND program contains courses and projects. The course will have fours parts:

### **Introduction to AI in Business**

First, we'll start by teaching you about the foundations of AI and machine learning: where is it used in industry and how do these technologies work? This section will discuss the type of data you need to create an AI product, the business cases that stand to benefit the most from AI-medicated technology, and the qualities of a good AI product team.

### **Creating a Dataset**

In this section, you'll learn how to create your own, novel dataset using Figure Eight's data annotation platform. Data annotation is all about structuring your data such that a machine learning model can learn to automatically find patterns within that data. Here, you'll learn the best design practices for creating a dataset of your own.

### **Build a Model**

In this section, you'll see how to build and train and end-to-end deep learning model to recognize patterns in a medical image dataset. You'll look at metrics that define the success of your trained model and parameters that affect how it trains.

### **Measuring Business Impact**

In this final section, you'll learn how to measure the efficacy of your model after it is released. This section discusses methods for identifying bias, updating a model in response to underlying changes in the data, and end-to-end case studies that demonstrate how AI products are ever improving and evolving.

There will be three projects to complete:

### **Project 1: Create a Medical Image Annotation Job**

In this project, you will design a data annotation job for a dataset of chest xray images; some of which contain signs of pneumonia. Your goal, as a product owner is to build a product that helps doctors quickly identify cases of pneumonia. As such, this project is designed to test your ability to build a labeled dataset that distinguishes between healthy and pneumonia x-ray images.

### **Project 2: Build a Model**

Take the next step and build a complete classification model that would serve as the backbone for a medical image classification product. (Don't worry, there's no coding involved!) For this task, you will use Google AutoML, an automated machine learning tool that will allow you to build the model and host it in the cloud. You'll measure the performance of multiple different models and evaluate them.

### **Project 3: Create an AI Product Business Proposal**

Put everything together in this final project; develop a complete business proposal for an AI product. The proposal will think through data considerations, evaluation metrics for a trained model, and design best practices for developing an AI product.

## Lesson 2 - Introduction to AI and ML

Most of the images pertaining to this section is in the corresponding folder.

### Supervised vs Unsupervised Learning

When you are thinking about using machine learning to solve a task, the type of algorithm you’ll use will generally depend on the data you are given. Before approaching a task, you should ask two questions: Does the data contain labels, such as true classes? Is the data continuous?

It may be helpful to consult the matrix below that addresses all kinds of data analysis cases.

* Discrete data is data that you can count and it has a finite amount, say the number of image classes or clothing item types.
* Continuous data is often numerical data that takes a large range of values.

## Lesson 4 - Using AI and ML in Business

### 1. Overview

Some successful business application areas of AI

![Business Applications](Introduction&#32;to&#32;AI&#32;in&#32;Business/Applications&#32;of&#32;AI.png)

### 2. AI Approach

A typical AI/ML training pipeline used by many ML teams to start building products.

![AI/ML pipeline](Introduction&#32;to&#32;AI&#32;in&#32;Business/AI&#32;Approach.png)

But, the most important point is to start from business problem and not data. It is important to get business value out of the AI product. Below is the AI approach which starts with the business problem.

![AI approach with business value](Introduction&#32;to&#32;AI&#32;in&#32;Business/AI&#32;Approach&#32;with&#32;Business&#32;Value.png)

Successful applications start with business problem which might take months refining.

**Business problem is the hardest part by far.**

Narrowly defining the business scope often leads to successful business applications.

*Most of the AI applications stall after the modelling phase where the model sits on the shelf rather than getting deployed.*

It is important that as a product manager you have a clear path to deploying the model in production systems as only then you can realize the business value.

### 3. Business Needs

*To reiterate, it is important to start with the problem and not the data.*

    It is most important that production systems have an active dynamic learning pipeline which learns frequently and benchmarks against a gold standard and updating that gold standard dynamically as the nature of the unstructured data changes in reality.

Typically you will need a human-in-the-loop process to achieve this.

![Production systems](Introduction&#32;to&#32;AI&#32;in&#32;Business/AI&#32;Production&#32;Systems.png)

### 4. The Business Case

An approach that realizes business value starts with the problem. An example use case is Adobe Stock. Lets get into the mind of one of the client of Adobe Stock. Here is an example use case:

![Adobe Stock use case](Introduction&#32;to&#32;AI&#32;in&#32;Business/Adobe&#32;Stock&#32;use&#32;case.png)

Here steps 5-8 could be accomplished using ML.

![Adobe Stock use case ML](Introduction&#32;to&#32;AI&#32;in&#32;Business/Adobe&#32;Stock&#32;use&#32;case&#32;ML.png)

The reason why this is a good problem for ML is there is a clear sense of what is to be accomplished and also there are lots of data available. Also we have a previous job that is tedious and impossible for humans to do in a realistic time frame.

Another tool that can help understand the business problem is identifying the AL value for the use case that need to be accomplished by the user.

![AI Value](Introduction&#32;to&#32;AI&#32;in&#32;Business/Identify&#32;AI&#32;Value.png)

### 5. Project Statement

As a product manager it is really important that we state to the stakeholders what problem we are solving. For that we have to develop a problem statement.

![Project Statement](Introduction&#32;to&#32;AI&#32;in&#32;Business/Project&#32;Statement.png)

### Breaking it All Down

Breaking a business problem to a narrow and specific problem is very critical for success of the project.

![Narrowing business problem](Introduction&#32;to&#32;AI&#32;in&#32;Business/Narrowing&#32;the&#32;business&#32;problem.png)

For example, in the case of home depot, it was found that product pictures with a white background had a better conversion rates than product images with normal backgroud.

![Product images](Introduction&#32;to&#32;AI&#32;in&#32;Business/Product&#32;images.png)

Another example of narrowing the business problem is using computer vision to look for empty shelfs ffor restocking items.

![Narrowing business problem 2](Introduction&#32;to&#32;AI&#32;in&#32;Business/Narrowing&#32;the&#32;business&#32;problem&#32;2.png)

As seen through the examples, it is very important to state the business problem we are trying to solve in oder to develop sucessful machine learning products.

![Using AI in business](Introduction&#32;to&#32;AI&#32;in&#32;Business/Using&#32;AI&#32;in&#32;business.png)

    We need to make sure that we are deploying for a very targeted narrow specific use case that has measurable business outcomes. It is important to start with business problem than the data.

    Success depends on data. Our AI tools are only as good as the data we put in them. It our data is bad, our ML tools are useless.

### Metrics

So how do we measure success? Metrics! Metrics! Metrics!
What is a good metric? There is no one correct answer.

![Metrics](Introduction&#32;to&#32;AI&#32;in&#32;Business/Metrics.png)

So what is the right metric for Adobe Stock images use case?

![Metrics Adobe use case](Introduction&#32;to&#32;AI&#32;in&#32;Business/Metrics&#32;Quiz.png)

So there is no one correct answer here. All of them sould serve as a useful metric for success. It depends on what metric is most meaningful to Adobe's business overall.

Another example for a business use case is LinkedIn which can be seen in the image below.

![Metrics LinkedIn](Introduction&#32;to&#32;AI&#32;in&#32;Business/Metrics&#32;LinkedIn.png)

### Need AI

Not all projects are well suited for AI and ML for their implementation. Some key considerations to look for AI projects.

![AI considerations](Introduction&#32;to&#32;AI&#32;in&#32;Business/AI&#32;key&#32;considerations.png)

The requirement of data is a key consideration for any AI project. The image below contains some questions to ask regarding the quality of data we have.

![AI data](Introduction&#32;to&#32;AI&#32;in&#32;Business/AI&#32;data.png)

Spending time with the dataset and actively looking at samples of data is critical to the role of product manager.

### Need AI Example

When using AI, the approach we should use really depends on the type of problem we are solving and the dataset available to us.

![ML vs DL](Introduction&#32;to&#32;AI&#32;in&#32;Business/ML&#32;vs&#32;DL.png)

A deployed AI system actually learns from production data and we can deploy piplines to evaluate its confidence levels.

![ML pipelines](Introduction&#32;to&#32;AI&#32;in&#32;Business/ML&#32;pipelines.png)

It is a best practice to incorporate actual humans into the learning pipelines so that we can update the model as new data becomes available and its performance in production.

### Things to Remember

![Things](Introduction&#32;to&#32;AI&#32;in&#32;Business/Things.png)

Another example use case is using ML chatbots for front line customer support.

![Business Case](Introduction&#32;to&#32;AI&#32;in&#32;Business/Business&#32;Case.png)

As is often the case, there is no magic solution for this, we nedd to start small with simple use cases and then iterate over to add additional use cases.

### ML Teams

It is one thing to develop models on our laptop and another thing to deploy production level ML models with thousands of users.

![Team needs](Introduction&#32;to&#32;AI&#32;in&#32;Business/Needs&#32;of&#32;Team.png)

In reality, ML teams needs to be cross funtional in order to have successful business outcomes.

![Cross funstional teams](Introduction&#32;to&#32;AI&#32;in&#32;Business/Cross&#32;funtional&#32;teams.png)

### Key Roles

Product Owner

![Product Owner](Introduction&#32;to&#32;AI&#32;in&#32;Business/Product&#32;Owner.png)

Designer

![Designer](Introduction&#32;to&#32;AI&#32;in&#32;Business/Designer.png)

Software Engineer

![Software Engineer](Introduction&#32;to&#32;AI&#32;in&#32;Business/Software&#32;Engineer.png)

Data Engieer

![Data Engineer](Introduction&#32;to&#32;AI&#32;in&#32;Business/Data&#32;Engineer.png)

Data Scientist

![Data Scientist](Introduction&#32;to&#32;AI&#32;in&#32;Business/Data&#32;Scientist.png)

Quality Assurance

![Quality Assurance](Introduction&#32;to&#32;AI&#32;in&#32;Business/Quality&#32;Assurance.png)

DevOps

![DevOps](Introduction&#32;to&#32;AI&#32;in&#32;Business/DevOps.png)

### Project Management

How much time it should take to deploy an ML solution really depends on the complexity of the business problem we are trying to solve. It is strongly recommended to use scrum as this is a iterative approach.

![Time](Introduction&#32;to&#32;AI&#32;in&#32;Business/Time.png)

Executing an ML project.

Executing an ML project using Scrum is similar to the normal development projects where we have spring backlogs and review meetings.

![Scrum](Introduction&#32;to&#32;AI&#32;in&#32;Business/Scrum.png)

### Summary

The picture below summaries the main points in this section.

![Summary](Introduction&#32;to&#32;AI&#32;in&#32;Business/Summary.png)
