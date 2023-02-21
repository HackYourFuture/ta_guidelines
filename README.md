# Technical assignment guidelines
At some point during the interview process for a software developer you will very likely be asked to do a technical assignment. This is a small exercise that the company has designed to test out your coding skills. This could be anything from solving some smaller tasks to building a simple widget to building a full stack project. The idea of the assignment is to see how you would solve a certain problem within a certain time constraint so that they know what you are capable of. Afterwards, there will be a followup interview scheduled with one of the developers as well to discuss your code. This is to ensure that you can discuss higher level concepts and see how you respond to feedback. By hiring a junior the company is investing time into developing your skills so they want to make sure that this is possible.

At HackYourFuture we practice this process multiple times during the curriculum to give you an idea of how it works. In this repository we will give you some guidelines to increase your chances of success in the technical assignment and interview afterwards.

## Technical assignment
There is a huge variety of technical assignments out there as it depends on what the company finds most important. The most popular assignment, however, is to build a small project that adheres to certain requirements. For example, you may have to build a dropdown that has search-as-you-type functionality or a frontend to an API provided by the company based on an design given in the assignment. The following tips are independent of the type of assignment, but should help to successfully complete the assignment.

### 1. Plan out your project
It is very tempting to dive in and start programming, but it is important to think ahead. There is a time constraint and at some point you will run into unforeseen problems so make sure you have the requirements of the project done as soon as possible. Any extra time after completing the requirements can then be spent on creating extra features. If something goes horribly wrong with adding a feature you then still have a version ready to show. It is always better to have something small completed that fulfils the requirements than a huge project that does not. The requirements are there because they want to see you tackle a certain problem, so make sure you actually tackle that problem.

For example, if you would get the assignment to build a todo list with the following requirements:

```
- Should be able to tag the todo items
- Should be able to search the todo items on the tags
```

The plan to implement this could be:

```
MUST-HAVE
1. Create the project structure
2. Create the schema for the todo items
3. Create an endpoint to get all the todo items
4. Create a page to view the todo items
5. Create an endpoint to add and remove tags to todo items
6. Add the ability to view the tags on the todo items on the frontend
7. Add the ability to add a tag to a todo item on the frontend
8. Add a button to remove a tag on a todo item on the frontend
9. Add a parameter to the get todo items endpoint that filters the todo items on tags
10. Add an input to the frontend that is sent to the get todo items input
11. Prepare the repository

NICE-TO-HAVE
- Add a feature that if you click on a tag it filters all the todo items for that tag
- Make the input for the filtering a dropdown so that the user does not need to type anything
```

Note that none of it is technical, you do not have to make any technical decisions here. You want to get a global overview in your head of what your project will contain and how you are going to get there. It will also help with the next step, discussing your plan!

### 2. Discuss your plan with a colleague
Unfortunately our experience shows that the descriptions of the technical assignments are not always very clear. This means that it is a good idea to show the requirements to someone else and then share your plan with them. If they interpreted a certain requirement differently this is a good time to ask the company to clarify what is meant. Asking these questions is actually positive, it shows that you think ahead and want to have clarity before starting a task. In your job this is called the `refinement` step.

Of course if you both see it the same way then it is time to get started!

### 3. Use git and commit your steps!
By making a project plan you not only ensure you are working on the right things, but it will also help you determine your commits. During the start of our curriculum you work alone a lot and on very small problems so it is natural to only work locally. Because of this many students at the beginning see git and committing as something you only do when you want to show the code to someone else, but commits actually allow you to structure your work. After completing a step in your plan, commit your code and then start on the next one. This way of working not only protects you from not being able to go back a step if you make a mess, but it also shows the people at the company that you work in a structured way.

### 4. Make the app look good!
Even though you should be judged on the code, the look of the app is actually the first impression of your application and everyone knows how important a first impression is. We have a whole repo dedicated to teaching you the basics of design [here](https://github.com/HackYourFuture/design_guidelines) so that you can make sure that your assignment gives off a good first impression. Follow those guidelines!

TIP: A good rule is to use the company's brand and colour palette when applying to a position!

### 5. Make the code look good!
If the app is your first impression, the code style is a strong second. Beautiful, good looking, production ready code is not only easier to read, but also gives off that professional vibe that you want to show. You will want to do a quick refactor/code style check after completing every step in your plan, but also make sure to do one last look through at the end to find anything you have missed. Check the following:

- No commented out code
- No unnecessary `console.log`'s
- Check your formatting. You should have the [prettier](https://scottsauber.com/2017/06/10/prettier-format-on-save-never-worry-about-formatting-javascript-again/) extension set up to do this for you automatically
- Check the naming of your functions and variables with the [naming conventions](https://hackyourfuture.github.io/study/#/programming/naming-conventions)
- No identical code in multiple places. Remember the [DRY principle](https://hackyourfuture.github.io/study/#/programming/dont-repeat-yourself)
- Add comments to code that is unclear or not logical. Sometimes there are exceptions needed that may need some explanation to a reader, add this to the code in a comment

You want to show you can create code that can go into production, so make sure your assignment follows these rules.

### 6. Prepare the repository!
Something that is often forgotten is the repository itself. The `README` is either empty or is the default one that comes with the `create-react-app` command. As a reviewer you will generally only get a link to the repository, which meanst that the `README` should help you get started. Before you hand in your application make sure the reviewer can find any information they need in the `README` file. The type of assignment indicates the information needed so there is not a single template, but in general make sure you have the following sections:

#### 6.1 Description
A small description to describe what the app does. You can make this a general description so that someone who may not have written the requirements also understands what the goal of the app is. This allows any other company that looks at your github to also see this assignment and understand what it does. Make sure to highlight the features that you may have built.

A good example of a strong description is the [node-chat](https://github.com/igorantun/node-chat#nodejs-chat) project. It has a couple of sentences at the top that introduces the app and the main technologies used. Then it has a screenshot of the application, which is nice to have in bigger projects, followed by a list of the key features.

##### 6.1.1 Demo
If the assignment is something that is deployable to the web then have a link to a working version in the `README` (like [WebApp](https://github.com/iharsh234/WebApp) does)! This makes it so much simpler to check out your application without having to go through the setup steps. There are many ways to deploy a project: if it is a static website then you can use [github pages](https://pages.github.com/), if it is a pure React application you can use [netlify](https://www.netlify.com/) and if it is a full application then [render](https://www.render.com/) is your best friend.

#### 6.2 Setup
There should be the list of commands to run to start your development environment. The reviewer should be able to clone your repo, run those commands and the app should be running on their computer. [Pomolectron](https://github.com/amitmerchant1990/pomolectron#how-to-use) has a very nice example of how to write it.

Make sure you test this setup by cloning your own repository in another folder and doing the steps. And if that works ask a friend or colleague to do the same! Your computer will have a lot of things set up that may not be set up the same way everywhere. Common problems you will not notice are:

- **Missing global packages.** 

A common problem is that you may have a package like `nodemon` installed globally on your computer. You cannot assume that the reviewer also has this installed so make sure that your setup only uses `node` or packages included in your `package.json`.

- **Missing environment variables.**

If your project requires certain API keys or other variables then create a `.env.example` file that indicates the variables needed. *NEVER* put your environment variables in a public git repository! If your app needs environment variables you can send your variables along in the e-mail to hand in your assignment, just do not put them in your codebase.

- **Uppercase letter != lowercase letter.**

Unix-based systems (Mac and Linux) are case sensitive where Windows does not care. So if you import a function from a file called `./MyFolder/MyFile.js` and you type `import { myFunction } from './myFolder/MyFile.js'` Windows will accept this, but a Mac will break. Make sure you check your naming or run a test on a Mac or Linux system to ensure that it works there too.

#### 6.3 Structure
If your assignment is bigger and you have created a folder structure it is common practice to explain this structure in the `README`. This gives the reviewer an indication of the architecture of your project and helps them understand the code. Below you can find an example of a technical assignment:

![image](https://user-images.githubusercontent.com/23367061/123788582-773fb280-d8dc-11eb-8ccb-799e7b41f869.png)

To get the structure you can use the `tree` command in your terminal or do it manually. It is not needed to have every file in there, just the overall structure.

#### Example repositories
The repositories below show some of the repositories that HackYourFuture students have made to hand in an assignment that are exceptionally good:
- [Salih TODO app](https://github.com/salih18/MERN-Todo-App)
- [Claudia's Strolly app](https://github.com/claudiadewindt/Strolly)

## Technical interview
When you get a technical assignment you will generally also get a technical interview along with it. This is very similar to the technical interviews you will have in the curriculum with your Education Director. This interview will usually be fully focused on the code that you built, which means you can expect to get the following questions:

- **Could you take me through the code?** 

This is harder than it looks, but we will practice this during the curriculum. It is important to explain the architecture behind the code, rather than the lines. You are talking to a developer after all. A common approach is to start by going over the folder structure and then decide on a feature to go through in detail. If you are confident you can even ask the interviewer what feature they would like to talk about and then go through that!

- **Why did you structure your app in this way?**
- **Why did you decide to use the `<insert package name>` package?**
- **How did you solve `<insert problem>`?**

For these questions the goal of the interviewer is to find out your decision making process. As developers we have a lot of options so we need to be able to weigh these options. Try to give alternative solutions/packages/structures and give the advantage(s) that your choice gives over the alternatives. As you are very new to being a developer you may get a question where you are not even aware there are alternatives. In those situations it is fine to say that you have only encountered this structure/solution/package so far and wanted to work in something that you were comfortable with for the assignment. This should be a last resort though.

You can also ask the question back: `What would you have done?` or `Would you have used something else?`. This is great for your knowledge and allows you to learn while interviewing!

- **What would happen if `<insert scenario>` happens?**
- **If we want to add `<insert feature>` to the application? What would you need to change?**

These questions are there to check if you fully understand all the intricracies of your application and get into a discussion with you about more abstract concepts. There is no real way to prepare for this, you just need to know your application and how it is built. This is why you should make sure that when you are making it you understand every piece of code that you add to your assignment. It is fine to copy paste something from the internet, as long as you understand what it does!

## Practice makes perfect
Be prepared to do quite a few technical assignments after graduating as you need to be able to prove your skills as a junior and a technical assignment is not easy. Every developer has different things that they find important and just like there needs to be a social culture fit there also needs to be a coding culture fit. Following these guidelines will make the chance of success a lot higher though. 


