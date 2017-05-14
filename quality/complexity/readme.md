
# How to Manage Complexity in Software

Many of complexities are man made unintentionally by human cognitive weakness, such as short of memory, [7 +/- 2](https://en.wikipedia.org/wiki/The_Magical_Number_Seven,_Plus_or_Minus_Two).

### Side-topic: Complexity and Quality

As a common sense, when a thing is simple (in term of scope of feature/requirement and the number of developers getting involved.), quality-wise, it is hard to make it wrong, even it happens to get wrong, it is easy to fix it. For example, if you are writing a numeric calculator app, you are unlikely to run into multi-threading problem, compared with apps connecting to remote servers.

Comparatively consider this case below:
* a newly formed team of people work in a product;
* the existing code base is heterogeneity in programming languages and tool chains;
* the product has a dynamic and rich set of features,
* the product have to use many technologies, legacy and novel, home brewed and 3rd party;
* the product runs on variety of market, culture and geography, office and wilderness.

It is complicated and inherently hard for quality assurance. Complexity must worthy of being managed well, especially for the sake of product quality. Since this series of topic is on Quality, I will also address the topic of managing software complexity in architecture and coding practices to help.
