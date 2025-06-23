# AI-BASED-RECOMMENDATION-SYSTEM

*COMPANY* : CODETECH IT SOLUTIONS

*NAME* : MOHAMMAD YAASIR

*INTERN ID* : CT04DG683

*DOMAIN* : JAVA

*DURATION* : 4 WEEKS

*MENTOR* : NEELA SANTOSH

*DESCRIPTION* :

Explanation of AI-Based Recommendation System in Java

In this project, I developed a simple yet effective AI-based recommendation system using Java and a popular machine learning library called Apache Mahout. The goal was to build a working system that could suggest items to users based on their preferences — like a mini version of the recommendation engines used by Amazon, Netflix, or YouTube.

To keep things simple and beginner-friendly, I wrote the program in a single Java file named RecommenderApp.java. The system uses a technique called Collaborative Filtering, which means it makes recommendations based on what similar users have liked. It doesn’t require complex AI models or large datasets, which makes it ideal for learning and demonstration purposes.


---

How It Works

The system starts by reading a small CSV file (preferences.csv) that contains user ratings for different items. Each line in the file represents a user's rating of a particular item, for example:

1,101,4.0
2,103,5.0

This means user 1 gave item 101 a rating of 4.0, and user 2 rated item 103 with a 5.0.

I used Apache Mahout's built-in data model, FileDataModel, to load this data. Then, I used the PearsonCorrelationSimilarity method to find how similar users are to each other. This is done by comparing how users rated the same items — if two users tend to rate items similarly, they are considered similar.

Next, the code defines a user neighborhood, which is simply the group of users most similar to the current user. In this case, I picked the 2 nearest neighbors. Mahout uses this group to determine which items to recommend to a user by looking at what those similar users liked but the target user hasn’t rated yet.

For example, if user 1 hasn't rated item 103, but similar users have and rated it highly, the system will recommend item 103 to user 1.


---

Why Apache Mahout?

Mahout simplifies the process of building recommendation systems. Instead of writing our own algorithms from scratch, we can use Mahout’s tested implementations. It handles things like similarity calculations, data models, and recommendation generation efficiently.

I chose Mahout version 0.9 because it includes a standalone Java library that works without needing a Hadoop setup or Maven configuration. This makes it easier to use in classroom projects or when you just want to learn the basics.


---

How to Run It

To make sure it works easily, I avoided Maven or IDEs. You just need:

The Java file (RecommenderApp.java)

The Mahout JAR file (mahout-core-0.9.jar)

A CSV data file (preferences.csv)


Then, you compile using:

javac -cp ".;mahout-core-0.9.jar" RecommenderApp.java

And run with:

java -cp ".;mahout-core-0.9.jar" RecommenderApp


---

Conclusion

This project shows how to build a basic AI recommendation engine using Java in a way that’s easy to understand and run. It’s a practical example of real-world AI concepts and gives a strong foundation to build more advanced systems, such as those using content-based filtering, hybrid models, or even deep learning in the future.


![Image](https://github.com/user-attachments/assets/e9d6c887-2d1d-4e0d-aa6a-1c8f3480f455)
