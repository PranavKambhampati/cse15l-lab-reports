# Week 5 Lab Report: Researching Commands

I chose to research the 'less' command. I will be exploring how we can use it in four different ways.

### Opening a file with the 'less' command

The 'less' command can be used to open and read the contents of a file. The benefit is that less will open the file within the terminal, however, it does so in a new page, so you won't be able to see the commands that were run. Here are examples of how less works after cd'ing into the right directory:

```
//Input
[cs15lwi23alz@ieng6-203]:Abernathy:243$ less ch1.txt

//Output (Note: a lot of text has been omitted as there is a lot of text in the chapter)

When people consider the U.S. apparel industry, they often think of New York City<E2><80><99>s Seventh Avenue, which is driven by new design, constantly changing seasonal offerings, and a willingness by consumers to pay a premium for the cutting edge of fashion. New York City and Los Angeles continue to have a competitive advantage in this area because a large number of designers and manufacturers are located in these cities and can respond quickly to changing demands, as well as shape them. This infrastructure allows for <E2><80><9C>quick response<E2><80><9D> on the fashion end of the women<E2><80><99>s and, to a more limited extent, men<E2><80><99>s markets. Once established, a variety of proponents believe, the experience at the fashion end can be diffused downward to less fashion-oriented products. As a result, some of the fashion-oriented products that had been sourced offshore can then return to the United States.

Finally, Chapter 15 (<E2><80><9C>Information-Integrated Channels<E2><80><9D>) touches on a number of public policy issues raised by our findings. These include what can be done about the continuing problem of sweatshops, the new international economics of trade, and the effect of information integration on the business cycle and consumer prices at the macroeconomic level. Last but not least, we take a realistic look at the competitive future of the U.S. retail, apparel, and textile industries.
The information-integrated channel, with its emphasis on time and product perishability, is the basis for our cautiously optimistic<E2><80><94>and unconventional<E2><80><94>outlook. Even more important, the forces examined in this book provide a glimpse into processes reshaping a considerable portion of the economy. Consumers no longer line up for a special suit at a store like Bond Stores; they also expect an ever more <E2><80><9C>fashionable<E2><80><9D> array of cereal products, computers, and automobiles. As the next chapter shows, the changes now under way have their roots in new technologies, just as technical advances in transportation and communication shifted the industrial landscape at the end of the last century.

```
In this example, after cd'ing into the right directory, the less command is able to open the file called ch1.txt to display all the text within that file. It does so in an editor that makes it relatively easy to navigate between lines. This is useful if we want to see the file without having to open it through the OS's GUI, especially if we were already in the terminal.
