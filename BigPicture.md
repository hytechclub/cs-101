# C# 101 Big Picture Code-Along Notes

I'm not sure if this is a "start" item, it's just an idea. It seemed like some of the kids were wanting more examples/an understanding of a concept's broader use. I was thinking maybe the code along each week, instead of being one-off prompts, could be parts of the same program. So maybe like the start of a dungeon game. For the week we cover readline/writeline, have the code along gather user input (name, favorite color) and write output ('Oh no, [username], you've been captured by a dark wizard! He has taken away your enchanted [color] sword and thrown you in a dungeon!' Then each week build on that, like for ifs we modify the program to allow a choice whether you're going to be a mage or warrior or something, so each week the new concept is the only unfamiliar part of the code and they have some context around what this new concept brings to the program.

Challenges
- Students missing a lesson
- Forcing topics into project
- Timing with other parts of lessons - staying on track
- Keeping separate from original lesson plans
- Keeping student project customizations - staying on track

Benefits
- Students have better context for why programming tools are used
- Students are familiar with parts of code so it's not all new each time
- Clayton has talked about the "big picture" for years - easier for people to follow along

Process
- Create final version of the project
- Build out individual weeks as steps for project
  - Have starting point for each lesson be ending point of previous lesson
- Fit project in with the other portions of each lesson (powerpoint, kahoot, etc)

Plan
- Should take 2-3 weeks
- May be worth doing
- Deadline - Nov 5
- Present milestones during stand-ups
- Follow-up with Michelle during it

## Options
### Choose Your Own Adventure
For this option, build a choose-your-own adventure game.

#### Architecture
- `while` loop for each turn, continue until player health is 0 or monster is defeated
- methods for attacking and defending and reading story
- conditionals for choice each turn

#### Increments
- Start with printing out colors and starting stats
- Next, ask user for name and weapon of choice
- Next, ask the user which option they choose (barn/forest)
  - going into the barn can give them a shield with higher defense, going into the forest fights the monster, etc
- player can attack mushrooms, may be attacked
- Next, allow them to make multiple decisions in sequence with a while loop
- Next, add more options that use methods (e.g. read story, maybe attack)

### Store
For this option, build a store that has transactions. It can be an economy simulator - the prices will be randomized each time.

#### Architecture
- `while` loop for each day at the market, continue until player quits
- methods for printing stats, printing items
- conditionals for choice on what to buy (one of two items, or nothing)

#### Increments
- Start with printing out colors and inventory and money
- Next, ask user for name and ask them what item to buy and how many (end of program)
- Next, calculate price for which item they choose (conditional)
- Next, loop it so they can come back to the market each day
  - Count the day
  - Randomize the prices
  - Keep track of users money and number of items they own
- Advanced: let the user sell back items
- Methods: cleanup code, read store rules