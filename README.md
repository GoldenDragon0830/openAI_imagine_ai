# ComfyUI Portrait Master

This node was designed to help AI image creators to generate prompts for human portraits.

## Available Options

- **shot**: sets the shot
- **shot_weight**: sets the coefficient (weight) of the type shot
- **hairs_style**: hairstyle selector
- **disheveled**: coefficient (weight) of the disheveled effect
- **nationality_1**: sets the first ethnicity
- **nationality_2**: sets the second ethnicity
- **nationality_mix**: controls the mix between nationality_1 and nationality_2, according to the syntax [nationality_1: nationality_2: nationality_mix]. This syntax is not natively recognized by ComfyUI; we therefore recommend the use of [comfyui-prompt-control](https://github.com/asagi4/comfyui-prompt-control)
- **age**: the age of the subject portrayed
- **freckles**: coefficient (weight) of freckles
- **skin_details**: coefficient (weight) of the skin detail
- **skin_pores**: coefficient (weight) of skin pores
- **moles**: coefficient (weight) for the presence of moles on the skin
- **skin_imperfections**: coefficient (weight) to introduce skin imperfections
- **eyes_details**: coefficient (weight) for the general detail of the eyes
- **iris_details**: coefficient (weight) for the iris detail
- **circular_iris**: coefficient (weight) to increase or force the circular shape of the iris
- **circular_pupil**: coefficient (weight) to increase or force the circular shape of the pupil
- **prompt_start**: portion of the prompt that is inserted at the beginning
- **prompt_additional**: portion of the prompt that is inserted at an intermediate point
- **prompt_end**: portion of the prompt that is inserted at the end

The node generates an output string. The generated text can then be used flexibly within your preferred workflow.

## Instal

To install comfyui-portrait-master in addition to an existing installation of ComfyUI, you can follow the following steps:

1. open the terminal on the ComfyUI installation folder
2. digit: `cd custom_nodes`
3. digit: `git clone https://github.com/florestefano1975/comfyui-portrait-master`
4. restart ComfyUI

## Customizations

The _lists_ subfolder contains the .txt files that generate the lists for some node options. You can open files and customize voices.

## Workflow

The [_prompt-master-sample-workflow.json_](https://github.com/florestefano1975/comfyui-portrait-master/blob/main/prompt-master-sample-workflow.json) file contains a basic workflow to immediately test how the node works.

![Example workflow](/screenshot/comfyui-prompt-master-01.png)

The [_prompt-master-sample-workflow.json_](https://github.com/florestefano1975/comfyui-portrait-master/blob/main/prompt-master-prompt-control-workflow.json) file contains a basic workflow with the prompt-control node.

![Example workflow](/screenshot/comfyui-prompt-master-07.png)

## Notes

When the generation of an image is started in the console you can read the complete prompt created by the node.

The effectiveness of the parameters depends on the quality of the checkpoint used.

For advanced photorealism we recommend [FormulaXL 2.0](https://civitai.com/models/129922?modelVersionId=160525).

## Practical advice

Using high values for the skin and eye detail control parameters may override the setting for the chosen shot. In this case it is advisable to reduce the parameter values for the skin and eyes.
