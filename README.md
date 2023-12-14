# ComfyUI Portrait Master

This node was designed to help AI image creators to generate prompts for human portraits.

![ComfyUI Portrait Master Node](/screenshot/comfyui-portrait-master-node.png)

## Instal

To install comfyui-portrait-master in addition to an existing installation of ComfyUI, you can follow the following steps:

1. open the terminal on the ComfyUI installation folder
2. digit: `cd custom_nodes`
3. digit: `git clone https://github.com/florestefano1975/comfyui-portrait-master`
4. restart ComfyUI

## Update

To install comfyui-portrait-master in addition to an existing installation of ComfyUI, you can follow the following steps:

1. open the terminal on the ComfyUI installation folder
2. digit: `cd custom_nodes`
3. digit: `cd comfyui-portrait-master`
4. digit: `git pull`
5. restart ComfyUI

## Available Options

- **shot**: sets the shot type
- **shot_weight**: coefficient (weight) of the shot type
- **gender**: sets the character's gender
- **nationality_1**: sets first ethnicity
- **nationality_2**: sets second ethnicity
- **nationality_mix**: controls the mix between nationality_1 and nationality_2, according to the syntax [nationality_1: nationality_2: nationality_mix]. This syntax is not natively recognized by ComfyUI; we therefore recommend the use of [comfyui-prompt-control](https://github.com/asagi4/comfyui-prompt-control). _This feature is still being tested_
- **facial_expression**: sets the character's expression
- **facial_expression_weight**: coefficient (weight) of the expression
- **face_shape**: sets the character's face shape
- **face_shape_weight**: coefficient (weight) of the face shape
- **facial_asymmetry**: coefficient (weight) to set the asymmetry of the face
- **hairs_style**: hairstyle selector
- **disheveled**: coefficient (weight) of the disheveled effect
- **age**: the age of the subject portrayed
- **skin_details**: coefficient (weight) of the skin detail
- **skin_pores**: coefficient (weight) of the skin pores
- **dimples**: coefficient (weight) for controlling facial dimples
- **freckles**: coefficient (weight) of the freckles
- **moles**: coefficient (weight) for the presence of moles on the skin
- **skin_imperfections**: coefficient (weight) to introduce skin imperfections
- **eyes_details**: coefficient (weight) for the general detail of the eyes
- **iris_details**: coefficient (weight) for the iris detail
- **circular_iris**: coefficient (weight) to increase or force the circular shape of the iris
- **circular_pupil**: coefficient (weight) to increase or force the circular shape of the pupil
- **prompt_start**: portion of the prompt that is inserted at the beginning
- **prompt_additional**: portion of the prompt that is inserted at an intermediate point
- **prompt_end**: portion of the prompt that is inserted at the end

Parameters set to 0.00 are not included in the prompt generated by the node.

The node generates an output string. The generated text can then be used flexibly within your preferred workflow.

## Customizations

The _lists_ subfolder contains the .txt files that generate the lists for some node options. You can open files and customize voices.

## Workflow

The [_prompt-master-sample-workflow.json_](prompt-master-sample-workflow.json) file contains a basic workflow to immediately test the node.

![Example workflow](/screenshot/prompt-master-sample-workflow.png)

The [_prompt-master-sample-workflow-prompt-control.json_](prompt-master-sample-workflow-prompt-control.json) file contains a basic workflow to immediately test the node.

![Example workflow](/screenshot/prompt-master-sample-workflow-prompt-control.png)

## Notes

When the generation of an image is started in the console you can read the complete prompt created by the node.

The effectiveness of the parameters depends on the quality of the checkpoint used.

For advanced photorealism we recommend [FormulaXL 2.0](https://civitai.com/models/129922?modelVersionId=160525).

## Practical advice

Using high values for the skin and eye detail control parameters may override the setting for the chosen shot. In this case it is advisable to reduce the parameter values for the skin and eyes.
