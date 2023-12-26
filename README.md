<a name="readme-top"></a>

# CuisineSync - Work in Progress
<br />
<div align="center">
  <a href="https://github.com/[Your_Github_Username]/CuisineSync">
    <img src="https://files.oaiusercontent.com/file-0pzilhilhsSGJbG1Txj652Mp?se=2023-12-26T03%3A31%3A38Z&sp=r&sv=2021-08-06&sr=b&rscc=max-age%3D31536000%2C%20immutable&rscd=attachment%3B%20filename%3Dfc40d0a5-25dc-42ce-bcf5-8a74714c9b11.webp&sig=lMsYBwxWPt7k/iP36zHpWJenUt%2BlPnPAF2e%2Bs8bdaqM%3D" width="600" height="600">
  </a>

  <h3 align="center">CuisineSync: Where Taste Meets Harmony</h3>

  <p align="center">
    Simplifying restaurant selection for group dining by addressing the challenge of indecision.
    <br />
    <br />
    <br />
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li><a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
      </ul>
    </li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

CuisineSync is an innovative app designed to enhance the group dining experience by making it seamless and enjoyable. It addresses the common problem of indecision when dining out with friends by offering a platform where group members can rank their favorite cuisines and set their budget. Our algorithm, powered by machine learning principles, then recommends the best restaurants that cater to the collective preferences.

### Built With

This section lists the major frameworks and services used to bootstrap CuisineSync.

* ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
* ![MongoDB](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
* ![Amazon AWS](https://img.shields.io/badge/Amazon_AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
* ![AWS SageMaker](https://img.shields.io/badge/AWS_SageMaker-FF9900?style=for-the-badge&logo=Amazon%20AWS&logoColor=white)

This section explains the technologies chosen for developing CuisineSync and the reasons behind their selection.

#### Java
* **Versatile and Robust:** Java's strong memory management and rich collection of libraries make it ideal for developing complex server-side applications. Its platform-independent nature allows for greater flexibility across different operating systems.
* **Team Proficiency:** The choice of Java was also influenced by the fact that most members of the project team are familiar with it, which streamlines development and collaboration, ensuring a higher quality and maintainability of the codebase.

#### MongoDB
* **Scalable and Flexible:** As a NoSQL database, MongoDB provides high performance, easy scalability, and a schema-less design, making it perfect for handling the varied and dynamic data associated with user preferences and restaurant information.

#### Amazon AWS
* **Reliable and Extensive Services:** AWS offers a broad set of global cloud-based products including storage, databases, analytics, and machine learning. Its reliability and scalability support the growth of applications from prototypes to full-scale deployment.

#### AWS SageMaker
* **Streamlined Machine Learning Workflow:** SageMaker enables developers to quickly build and train machine learning models and deploy them into a production-ready hosted environment. This aligns well with CuisineSync's need for a robust recommendation system based on user preferences.


## System Design and Overview
![System Design](https://github.com/wburayu/CuisineSync/assets/92478988/23c36a86-9485-460b-9f83-e631958ec838)
### Frontend
- **Interface & Interaction**: The frontend is the user-facing component of CuisineSync. It's designed to capture user inputs, such as registration details and preference selections, providing an intuitive and interactive experience.

### Backend - Handle APIs
- **API Management**: This backend layer is responsible for handling API requests from the frontend, including:
  - `GET /users/{userid}`: Retrieve user details.
  - `POST /users/{userid}`: Create new users or update user preferences.
  - `GET /match/{body}`: Handle matching operations that likely involve comparing user preferences.

### Backend - Matching Service
- **Preference-Based Matching**: This service processes user IDs to retrieve a tailored list of restaurant recommendations, utilizing a combination of user and restaurant documents to perform the matching logic.

### SQL Database
- **Structured Data Storage**: A relational database setup to store and manage structured user data. It comprises tables such as:
  - `Users`: Contains columns like `user_id`, `username`, `preference_id`.
  - `Preferences`: Holds `preference_id`, `location`, `noodle_score`, etc.

### NoSQL Database (MongoDB)
- **Flexible Data Management**: MongoDB is employed as a document-based database to store flexible, semi-structured data, which includes:
  - User documents: With fields such as `userid`, `username`, `noodle_score`.
  - Restaurant documents: With details like `rest_id`, `name`, `location`, `noodle_score`.

### Machine Learning Component
- **Data-Driven Recommendations**: This component applies machine learning algorithms to populate restaurant documents with scores, reflecting the compatibility of each restaurant with the user preferences, which are then used to provide ranked recommendations.

### Data Flow
- **System Integration & Data Processing**: The frontend communicates with the backend via API requests, sending and retrieving user information. The Handle APIs layer works in conjunction with both SQL and NoSQL databases to manage user data effectively. The Matching Service leverages this data to offer restaurant suggestions, while the machine learning component enriches the database entries with predictive scoring.

### Architectural Philosophy
- **Separation of Concerns**: CuisineSync's design embodies a clear separation of concerns, with each service dedicated to a specific aspect of the application's operation, ranging from user management to intelligent data processing and retrieval.

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

List of things you need to use the software and how to install them.

* Java
* MongoDB
* AWS Account

## Roadmap

- [x] Conceptualize the core functionality of the app
- [ ] Design the database schema for user preferences.
- [ ] Develop the machine learning algorithm for restaurant recommendations.
- [ ] Implement a basic user interface.
- [ ] Integrate third-party APIs for restaurant data and location services.

## Acknowledgments

* [Java](https://www.java.com/)
* [MongoDB](https://www.mongodb.com/)
* [Amazon AWS](https://aws.amazon.com/)
* [AWS SageMaker](https://aws.amazon.com/sagemaker/)

