# Cellpose-batch-segmentation-and-counts

This was suggested to me as a solution for my egg segmentation issues from my post on the [Image.sc community forum](https://forum.image.sc/t/insect-egg-counts-help-any-ideas-on-how-i-can-segment-and-accurately-count-eggs/90643/16). If you havent checked out [Image.sc](https://forum.image.sc/) I would highly recommend it for anything pertaining to complex image analysis and computer vision, the community are very generous and helpful.

This is a batch processing script that utilises a pretrained [cellpose model](https://github.com/mouseland/cellpose) to identify and count eggs on filter paper of _Folsomia candida_, a springtail that has high reproductive output. 
Additionally, the script also contains some functions for pulling information from filenames that are saved along with egg counts. My image file names contain important information related to an experiment, for example: 

I1_F1_O20_SWI_R1_13-09-23 where I1 = isoline, F1 = generation, O = age, could be Y, 20 = temperature (could be 25 degrees), SWI = treatment (could be CON), R1 = replicate, and date. The script collects this data and adds the output to a csv to efficiently create a complete data set for further analysis.
The labels created from the cellpose model are saved to an output directly as images but are also saved overlayed over the original images (so one can inspect the result easily). 

The images I used for this script were initially segmented using [Meta's Segment Anything](https://github.com/facebookresearch/segment-anything) model to remove background from the shape of interest (In this case the filter paper containing springtail eggs). Please see my repository [here](https://github.com/wyldescience/Segment-anything-batch-process/wiki) if of interest or use to you. 
