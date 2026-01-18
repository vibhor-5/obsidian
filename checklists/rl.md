Assuming we are excluding Model-based RL (because that is for nerds/a different topic / kinda stupid).

I recommend:

1. Understand the basics, i.e. classical RL. Best case: Chapters ~1-9 from barto& Sutton
    
2. Solve at least half of the tasks and questions they offer.
    
3. Understand key algorithms in the field. Repeat reading the core paper(s), and then implementing the algorithm yourself for the following: List: DQN RAINBOW DQN (only implementing double-q and competing q for it) REINFORCE (not based on paper, but based on lillog post) A2C (implement), read A3C paper PPO (also read TRPO, but don't implement) (also read ICLR accepted Blogpost on how it is shaped by choices) DDPG TD3 SAC
    
4. Look into some topics beyond base algorithms, again read and implement some (marking my opinion on which to impl ment with an asterisk*), some below are algos, some topics.
    

HER * 2-3 basic Inverse RL papers World Models Paper* RIAL&DIAL paper by j. Foerster MADDPG* Intrinsic motivation (I like the two pathak papers for beginners) Offline RL (talk by s. Levine, not paper) Conservative QL

Then you can have a look at some more advanced/detailed stuff. I choose these for my students because they are interesting/contextualise the field: Mirror Learning AlphaGo (because now it's justified to actually look into some model based stuff and you really should know what MCTS is) RLHF IMPALA

Sorry for the mess, but I'm busy, and it's late now, and over the day I got research to do. The above is more or less the syllabus for the DRL course I teach. Basics-->Key algos --> papers representative of key subfields/topics. Mist important tip: Actually do implement things. People allways THINK they understand RL after reading some papers, until they actually implement and learn they actually don't really understand things. Implementing yourself is the only way to actually understand. Otherwise you are just like the drunk people screaming at their TV blasting football and thinking they could do that Imho.