# League of Legends Social Network
This project has two main components: the Reddit API scraper and the social network analysis. What I want to do is to construct a social network of playable characters (aka champions) based on how often the characters are discussed together by players.

### Project Goals
I was mostly concerned with developing my Python skills for this project. It also allowed me to develop new skills, like interacting with an API and working with regular expressions. I mainly chose League of Legends because it's a hobby of mine and that helped me stay interested. 

## Reddit API
First, I created a web scraper via the Reddit API in order to extract user comments on reddit. This can be applied in general to any subreddit, but for this project I will particularly be looking at [/r/summonerschool](http://www.reddit.com/r/summonerschool/). There is a lot of discussion in this subreddit so it seemed like a good place where champions would be mentioned a lot. 

## Social Network
I take the data gathered from Reddit, and search the text for which champions are being discussed. Since I have the comment trees in tact, I know which champions are being discussed in the same comment trees. This is important because it is reasonable to assume an underlying relation between champions being discussed in the same trees.

I am still working through the social network graph (tweaking the visualization), but the main idea is to connect champions that are mentioned frequently together. I expect to see clusters of champions appear based upon their in-game roles (certain champions are more likely to play in the same areas of the map). I also want to incorporate the champion's popularity too so this dimension can be explored as well. For instance, do popular champions tend to be clustered together?

## Next Steps
One technique I'd really like to incorporate is using a tool like plot.ly to allow me to update the network for desired champions. For instance, I can select a particular champion and see its neighbors update in real time.
