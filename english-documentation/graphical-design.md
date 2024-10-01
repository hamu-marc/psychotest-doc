# Graphical design

The edit mode includes a graphical interface for the design of screens (graphical design). This form of editing complements the commands in the command line . A screen structure needs to be set and stimuli have to be inserted prior to launching the graphical editor. After having inserted the screens, the graphical editor needs to be opened by clicking on the 'Graphical layout' tab above the command edit window.&#x20;

The graphical editor uses the graphical interface of the GrapeJs library. The workflow for working with the graphical editor is composed of individual consecutive steps and is therefor also overviwed in the followng paragraphs.&#x20;

## Setting the screen size

The first step includes a selection of the test screen size. It is recommended to set a smaller test screen if the test dedicated for use on mobile phones. The feature can also be used to verify the behavior of the test on different screens.

The options in each step can be undone or restored by clicking the according buttons. The screen can be imported or cleaned (delete). The graphical overview of the rendered design can be switched into full screen and its code can also be displayed using view code button.

## Setting the grid

The adjacent step of the workflow includes selecting the components in the graphical overview of the components using the following button. Clicking on the the blocs creates a grid wich can be enriched in response elements. The rows can be split into  1, 2, 3 collums and can be also split into two colums in the 3 / 7 ratio.&#x20;

## Placing the response elements

The following workflow step includes placing the response elements. These are the  `taskvalue` response fields, `taskscale`a categorical evaluation based on the defined numerical and verbal values or `ranking2d`scales which can be descirbed verbally, and the `stimulus` equivalent of `ranking2d` which allows a constant stimuli.

## Defining the response elements

The response elements need to be further defined using the 'Setting' tab. The tasks which can be further defined include  `taskedit`(name, colour),`taskvalues` (name, labels, values, distribution of colour), `taskscale` (pattern, name, minimum, maximum, step, descriptors, values, colour) `ranking2d` (name, stimuli randomisation, axis descriprion). Special graphical elements of graphical styles and layers can be also set (open style and layer manager).
