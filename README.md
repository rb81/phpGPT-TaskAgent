# phpGPT-TaskAgent
A playful experiment to get ChatGPT to identify and complete its own tasks.

## Introduction

This is a fun little experiment to see if I could get ChatGPT to create a list of tasks needed to accomplish a given mission. The biggest challenge was getting ChatGPT to identify tasks that it is capable of completing without human interaction or data outside of its own.

## Workflow

The application creates four separate agents, as follows:

1. **Role Identifier:** An agent to identify the system role needed to complete the given mission.
2. **Manager:** An agent to identify the tasks needed to complete the mission, based on the given role.
3. **Researcher:** An agent that is given one task at a time and asked to complete specific actions.
4. **Reporter:** An agent that is given all the data compiled by the Researcher and asked to provide a final output.

## Limitations

- The application only cycles through tasks once. Cycling through them multiple times, or creating other agents to perform some refinement, may produce better results.
- The process and preliminary outputs are not being saved or echoed. Only the final output is presented.
- The agents are only given a single system role which may be limiting. (Getting a role for each separate task may be better.)

## Dependencies

This application uses:

- [phpGPT](https://github.com/rb81/phpGPT) to connect to OpenAI's ChatGPT API
- [ParseDown](https://github.com/erusev/parsedown) to output the final result in beautiful HTML
