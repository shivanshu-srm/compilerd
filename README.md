# <img alt="Kalvium" src="https://kalvium.community/images/sidebar-2d-logo.svg" width="80"/> Kalvium

---

This template offers a streamlined configuration to set up React with Vite, ensuring seamless integration with Hot Module Replacement (HMR) and enforcing essential ESLint rules for code consistency.

Currently, the Vite ecosystem boasts two prominent official plugins tailored for React development:

- **[@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md)** leverages [Babel](https://babeljs.io/) to facilitate Fast Refresh, enabling rapid updates to React components during development cycles.

- **[@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc)** harnesses [SWC](https://swc.rs/) for Fast Refresh, enhancing performance by utilizing a speedy JavaScript/TypeScript compiler. This plugin optimizes React applications for efficiency and responsiveness, making it an excellent choice for projects prioritizing performance alongside developer productivity.

These plugins collectively elevate the development experience with Vite, enabling React developers to build modern, responsive web applications efficiently while adhering to best practices in code quality and live updates management.



Certainly! Here's an expanded version of the description message for your project:

---



I've made significant strides in enhancing the Code Judge project across several key areas:

1. **Language Expansion:** Introducing Ruby, Golang, and prompt-based evaluations (Promptv1 and Promptv2) has bolstered the project's capability to handle a broader range of programming languages, ensuring inclusivity and versatility.

2. **Comprehensive Test Coverage:** I've meticulously expanded the test suite to encompass a wide array of scenarios and edge cases. This thorough testing approach not only enhances reliability but also fortifies the project against potential pitfalls.

3. **Feature-Rich Frontend:** A well-crafted frontend interface, housed in its designated "frontend" folder, has been meticulously developed. This frontend empowers users with an intuitive platform to seamlessly compile and execute code across all supported languages, enhancing usability and accessibility.

4. **Custom Feature Integration:** In addition to foundational enhancements, I've introduced a bespoke feature aimed at augmenting the project's functionality. This addition reflects a commitment to continuous improvement and innovation in code evaluation capabilities.

These combined efforts underscore a holistic approach to improving the Code Judge project, equipping it with robust capabilities, rigorous testing standards, and a user-centric frontend experience.
<!-- [![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url] -->






## Table of contents : 
<ol>
  <li>
    <a href="#about-the-project">About The Project</a>
  </li>
  <li><a href="#quick-usage">Quick Usage</a></li>
  <li><a href="#contribution">Contribution</a>
    <ul>    
        <li><a href="#Prerequisites">Prerequisites</a></li>
    </ul>
    <ul>    
        <li><a href="#setting-up">Setting up</a></li>
    </ul>
    <ul>    
        <li><a href="#making-changes">Making Changes</a></li>
    </ul>
    <ul>    
        <li><a href="#running-tests">Running Tests</a></li>
    </ul>
    <ul>    
        <li><a href="#Guidelines">Guidelines</a></li>
    </ul>
  </li>
  <li><a href="#license">License</a></li>

</ol>



## About The Project : 
Compilerd is a online code judge for evaluating code submissions passed to it. It compiles and executes code in several languages and returns the result and various other properties in the response. The judge supports several languages including C++, Python, C, JavaScript (Node.js) and Java. 
This is a service that is build using nodejs and express in the backend.
It is fully customizable and can be adjusted as per requirement. Also, it has been tried and tested on Google Cloud Run and it just works seamlessly.


## Quick Usage :
We will run the project locally and try to make a request to see a sample use case :
  - Clone the repo : ```git clone <web-url>```
  - Change directory to the project's root folder.
  - Install dependencies : ```npm install```
  - Build docker image : ```docker build -t <tag> .```
  - Run the docker container with the built image : ```docker run -p 3000:3000 -e OPENAI_API_KEY=<your-api-key> -e ALLOWED_RAM=<allowed-ram-value> <image-name>```
  - Now we have the service running on localhost ```http://localhost:3000/```
  - Open postman and try to make a POST request on ```http://localhost:3000/api/execute/``` with given payload :
    ```json 
        {
            "language" : "nodejs", 
            "script" : "console.log('hello world')"
        } 
    ```
  - You should see something like this in the response : 
    ```json
        {
            "output": "hello world\n",
            "execute_time": null,
            "status_code": 200,
            "memory": null,
            "cpu_time": null,
            "output_files": [],
            "compile_message": "",
            "error": 0
        }
    ```

## Languages supported :
  - C
  - CPP
  - Python
  - Java
  - Node.js
  - Ruby

## Contribution :

### Prerequisites:
For local development we should have the following dependencies set up locally in our system
  - Nodejs : [nodejs](https://nodejs.org/en/download)
  - Npm : this comes automatically with nodejs installation
  - Docker : [docker](https://docs.docker.com/get-docker/)
  - Postman or alternative : [Postman](https://www.postman.com/downloads/)
  - Git : [Git](https://git-scm.com/downloads)


### Setting up :
  - Fork the repository using Github UI.
  - Clone locally from the forked repo.

### Making changes:
  - Make sure to create a new branch on top of the main branch : ```git checkout -b <name>```
  - After making changes we can commit them using ```git commit -am <commit-name>```


### Running tests : 
  - It is important to make sure that changes are not breaking, hence they should be tested aginst provided suite of test cases in repo.
  - Run the server in a docker container by using below commands :
    - ```docker build -t <tag-name> .```
    - ```docker run -p 3000:3000 -e OPENAI_API_KEY=<your-api-key> -e ALLOWED_RAM=<allowed-ram-value> <image-name>```
  - Execute the test script by running command ```node ./tests/test.js```
  - Summary can be seen on the console when all the tests have finished.



### Guidelines :
 - Provide Detailed Pull Requests
   - Clearly describe the problem you're solving or the feature you're adding
   - Provide context, background, and any relevant information
 - Adhere to the project's coding standards and style guides
 - Update documentation as needed for your changes
   - Ensure that your code is well-documented and easy for others to understand
 - Ensure that your contributions are well-tested
 - Maintain consistency with the existing codebase



<!-- LICENSE -->
## License : 



[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
