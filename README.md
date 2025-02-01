Social Media Feed Ranking Using Priority Queues:
This project implements a social media feed ranking system using Priority Queues to efficiently rank and display posts in a social media feed. The primary goal is to provide users with a personalized feed by sorting posts based on relevance, engagement, and other customizable metrics.

Features:
Priority Queue: Uses a priority queue to maintain and rank posts based on their importance or engagement level.
Customizable Ranking Metrics: Allows users to define how posts are ranked (e.g., likes, comments, time of post, user preferences).
Efficient Sorting: By leveraging priority queues, the system optimizes the process of sorting and ranking, ensuring that the most relevant posts are displayed at the top.
Scalable: Suitable for use in large-scale social media platforms where high volumes of data need to be processed.
    
How It Works:
A PriorityQueue is used to store posts, with each post's rank being dynamically adjusted based on its interaction metrics (e.g., likes and comments).
Posts are ranked by their priority, where higher-ranked posts appear first.
You can customize the ranking function to prioritize different aspects of the post (such as recency, likes, or comments).
Example
Here's an example of how to use the system:

python

from priority_queue import PriorityQueue
from post import Post
from feed_ranker import FeedRanker

# Create some sample posts
post1 = Post(id=1, timestamp='2025-02-01T12:00:00', likes=120, comments=45)
post2 = Post(id=2, timestamp='2025-02-01T13:00:00', likes=200, comments=75)
post3 = Post(id=3, timestamp='2025-02-01T14:00:00', likes=50, comments=10)

# Initialize the feed ranker and add posts
feed_ranker = FeedRanker()
feed_ranker.add_post(post1)
feed_ranker.add_post(post2)
feed_ranker.add_post(post3)

# Rank the feed based on a custom metric
feed_ranker.rank_feed()

# Display the ranked feed
ranked_feed = feed_ranker.get_ranked_feed()
for post in ranked_feed:
    print(f"Post ID: {post.id}, Likes: {post.likes}, Comments: {post.comments}")
    
