# League of Legends Social Network
This project has two main components: the Reddit API scraper and the social network analysis. What I want to do is to construct a social network of playable characters (aka champions) based on how often the characters are discussed together by players.

### Project Goals
I was mostly concerned with developing my Python skills for this project. It also allowed me to develop new skills, like interacting with an API and working with regular expressions. I mainly chose League of Legends because it's a hobby of mine and that helped me stay interested. 

## Reddit API
First, I created a web scraper via the Reddit API in order to extract user comments on reddit. This can be applied in general to any subreddit, but for this project I will particularly be looking at [/r/summonerschool](http://www.reddit.com/r/summonerschool/). There is a lot of discussion in this subreddit so it seemed like a good place where champions would be mentioned a lot. 

## Social Network
I take the data gathered from Reddit, and search the text for which champions are being discussed. Since I have the comment trees in tact, I know which champions are being discussed in the same comment trees. This is important because it is reasonable to assume an underlying relation between champions being discussed in the same trees.

For the network, the size of the node is proportional to the amount of times the champion was mentioned in comments. The network edges had to be filtered as well, as it was too difficult to visualize the graph if I included too many edges. The champions had to be mentioned in the same comment trees at least 11 times in order to have a connection drawn. 

## Plot.ly
After creating the network, I fed the data into plot.ly because the static image was rather difficult to interpret. This interactive plot can be panned and zoomed to better explore the data. Also, there are dropdown menus that can be selected to display only a particular champion and its direct neighbors. The final plot can be viewed below, or at [plot.ly](https://plot.ly/~zachturn/0/lol-champion-network/#plot)

<div>
    <a href="https://plot.ly/~zachturn/0/" target="_blank" title="LoL Champion Network" style="display: block; text-align: center;"><img src="https://plot.ly/~zachturn/0.png" alt="LoL Champion Network" style="max-width: 100%;width: 1000px;"  width="1000" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
    <script data-plotly="zachturn:0"  src="https://plot.ly/embed.js" async></script>
</div>

<iframe width="900" height="800" frameborder="0" scrolling="no" src="https://plot.ly/~zachturn/0.embed"></iframe>

