# Pavlovia Integration
Updated Pavlovia Integration instructions for lab.js and jsPsych

# lab.js 2023 version
1. Once you have coded your study using lab.js, use the "Export as integration" -> "Pavlovia" option.
2. Open your Pavlovia GitLab Repository page and upload the code (https://pavlovia.org/docs/experiments/overview)
3. The easiest way to do that is by creating an SSH key: https://gitlab.pavlovia.org/help/gitlab-basics/create-your-ssh-keys.md
4. Go to your dashboard and run your experiment from there
   
# jsPsych v7.1.2
1. Write your jsPsych study
2. Add the follwing line to the HTML part of your study:
```
<script type="text/javascript" src="lib/jspsych-7-pavlovia-2022.1.1.js"></script>
```
3. Add this routine as the first in your timeline:
```
var pavlovia_init = {
			type: jsPsychPavlovia,
			command: "init"
		};
		timeline.push(pavlovia_init);
```
4. Add this routine as the last in your timeline:
```
var pavlovia_finish = {
			type: jsPsychPavlovia,
			command: "finish",
			participantId: "JSPSYCH-DEMO"
		};
timeline.push(pavlovia_finish);
```
5. Open your Pavlovia GitLab Repository page and upload the code (https://pavlovia.org/docs/experiments/overview)
6. The easiest way to do that is by creating an SSH key: https://gitlab.pavlovia.org/help/gitlab-basics/create-your-ssh-keys.md
7. Go to your dashboard and run your experiment from there
