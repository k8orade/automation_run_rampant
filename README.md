# Automation Run Rampant

### RubyConf 2017
With the rise of micro services and DevOps culture, Ruby developers have suddenly found themselves responsible for the entire delivery pipeline of their services. That’s a lot of work when you’re responsible for a single service, and an unmanageable amount of work if you have any more than that. Luckily, many of these processes can be automated, and Ruby is a fantastic language to do it in! But where do you begin? How do you know when something is ripe for automation? Is there such as thing as bad automation? And, if you decide to automate something, how do you take the first step?


## Automation Tooling Patterns
### Swiss Army Knife
Combines multiple individual functions behind a single simple interface, to provide a kind of one-stop-shop for the development or delivery process.

Have a look at Kubernetes for an example.

#### Benefits
- Enables developers to perform their task as quickly as possible, without having to make too many decisions that might slow them down.
- They’re simple and intuitive to use, which means that developers won’t have to invest a lot of time in learning how to use them
- There’s only a limited number of ways that this tool can be interacted with, so its integration across all of your systems is going to be almost identical, making it easier for developers to move between these systems.

#### Drawbacks
- Adoption can be poor because these tools are very opinionated (i.e. the people wanting to use your tool might not agree with the mandates that it's imposing).
- Need to invest a lot of time to make it so obvious and easy to use, that there’s no reason for them not to use it.
- Need a lot of good support, so that any problems encountered using your tool are solved quickly and engineers don’t find their work blocked waiting for your automation tooling to work for their system.

### Screwdriver
This is a tool that focuses on solving just a single problem, so it’s very small in scope.

Have a look at Capistrano for an example.

#### Benefits
- Encourages innovation by enabling teams to take control of their own technical decisions so that they can move fast and experiment with new languages, tools or frameworks.
- More flexible and able to be used in a wider variety of situations. This is because they push a lot of decisions down to the developers.
- Easy to understand the mechanics of what the tool is doing because it focuses on a small scope of functionality and doesn't make many assumptions.

#### Drawbacks
- Results in duplicated effort as the same configuration work is done over and over by different engineers for different systems.
- Variance between systems in how the same automated step works, even though they’re all using the same tooling, because of the difference in configuration.
- Require knowledge from your engineers as they’ll be responsible for making the important decisions that the tool isn’t making.

### Duct Tape
Wraps an existing system to create a consistent interface.

Have a look at [Scripts to Rule Them All](https://github.com/github/scripts-to-rule-them-all) for an example.

#### Benefits
- Improved agility as the tool reduces the friction or overhead making changes.
- Faster to develop as the tools are generally small and have no business logic.

#### Drawbacks
- Can become obsolete very quickly, so either needs to be temporary or updated frequently as wrapped system changes.
- Questionable value. Wrapper can just end up obfuscating the underlying system and making it more difficult for engineers.
