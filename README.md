# News Aggregator V2

### Description 
For this assignment you have to implement an application that aggregates news from two different APIs. The APIs you'll be using are [**Reddit**](https://www.reddit.com/dev/api/ "Reddit") and [**News API**](https://newsapi.org/ "News API").

The application that you submit must have thoughtful design decisions, well documented and unit tested code. This assignment should not take more than 5 hours to complete.

### Functions
The two functionalities that need to be implemented are "list" and "search".

This is an example request for a generic GET request which should fulfill the "list".

```
> Request
GET /news   HTTP/1.1
Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ
Accept: application/json

> Response
[
  {
    "headline": "Human organs can be stored for three times as long in major breakthrough for transplants",  // Headline of the article
    "link": "https://www.telegraph.co.uk/science/2019/09/09/human-organs-can-stored-three-times-long-major-breakthrough/",  // Link of the article
    "source": "reddit" // Source that you retrieved this news from
  },
  {
    "headline": "Depth of Field: The Shared Memory of One World Trade Center",
    "link": "https://www.wired.com/story/one-world-trade-center-history-future/",
    "source": "newsapi"
  },
]
```

You should also implement a feature that allows someone to "search" through the news.

```
> Request
GET /news?query=bitcoin   HTTP/1.1
Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ
Accept: application/json

> Response
[
  {
    "headline": "IRS goes after cryptocurrency owners for unpaid taxes",
    "link": "https://www.cbsnews.com/news/own-bitcoin-irs-pursues-cryptocurrency-owners-for-unpaid-taxes/",
    "source": "reddit"
  },
  {
    "headline": "Skirting US sanctions, Cubans flock to cryptocurrency to shop online, send funds",
    "link": "https://www.channelnewsasia.com/news/business/skirting-us-sanctions--cubans-flock-to-cryptocurrency-to-shop-online--send-funds-11901148",
    "source": "newsapi"
  },
]
```

*Suggestion:* Try to use /r/news for Reddit and the general category for News API (you don't have to but it's worth checking out).

### Constraints
There are some constraints that you should be aware of. Not completing any of the following constraints will stop your candidacy from moving forward:
- You must use **Python**. 
- You must use [**FastAPI**](https://github.com/tiangolo/fastapi) for serving HTTP requests. This is to test your ability to design without the use of heavy frameworks.
- You cannot use [**PRAW**](https://praw.readthedocs.io/en/v2.1.21/) for the Reddit API.
- You cannot use any database technology to aid in your development (Redis or equivalent is fine).
- You must return the three fields that are in the sample requests above in JSON format. You can add more fields if you'd like.
- You must return fields from all APIs if any exist. Example: If API A and API B return something then the result of these two need to be shown in the final aggregated return. If I add API C I need to see the results of that API in the final aggregator return. If API C yields no results then you don’t have to show it.
- This needs to be a running Python application on your localhost that serves an HTTP request not a console application.

### Assessment
Primarily, we will be assessing good **design decisions**. To do this, we have a hidden API that we have written that has different specifications than the ones that have been provided above. We will be integrating my own API into your news aggregator. It needs to be a simple and clear integration, the simpler the better.

Secondly, we will be assessing good **application performance**. The overall speed of the application should not be affected by poor API speed. You need to be creative on how to solve this problem. *Suggestion: look into LRU caches.*

In addition, we will be assessing the following points:
- Python Proficiency
- Ability to understand and use 3rd party APIs
- Ability to parse different forms of data
- Ability to write unit tests
- Ability to write documentation
- Ability to follow SOLID principles
- Generally professional code that follows standards in matter of commits and security

### Submission
You should upload your code to a Github repository (private or public) and share it with me. Your repository should have a README.md that explains how to run the code and if you’ve done anything extra. **If you fail to produce this repository within the time period mentioned in the email you received your application will be rejected.**

Best of luck!

~ Meddy Team

