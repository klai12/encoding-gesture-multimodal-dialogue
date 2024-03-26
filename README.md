# Encoding Gesture in Multimodal Dialogue: Creating a Corpus of Multimodal AMR

This repository contains the corpus and annotation guidelines for the paper:

Kenneth Lai, Richard Brutti, Lucia Donatelli, and James Pustejovsky. 2024. Encoding Gesture in Multimodal Dialogue: Creating a Corpus of Multimodal AMR. In _Proceedings of LREC-COLING 2024_.

## EGGNOG Corpus

Our corpus is layered on top of the [EGGNOG corpus](https://www.cs.colostate.edu/~vision/eggnog/). The videos are not included here, but can be downloaded at the preceding link.

### Video Key

The following table maps labels used in this corpus to (signaler) videos in EGGNOG:

|Label|Video                                             |
|-----|--------------------------------------------------|
|p15  |s08/part2_layout_p15/20151120_211739_00_Video.avi |
|p16  |s08/part1_layout_p16/20151120_205959_00_Video.avi |
|p16_2|s08/part1_layout_p16/20151120_210259_00_Video.avi |
|p17  |s09/part2_layout_p17/20151202_221714_00_Video.avi |
|p18  |s09/part1_layout_p18/20151202_220401_00_Video.avi |
|p19  |s10/part2_layout_p19/20151203_234805_00_Video.avi |
|p20  |s10/part1_layout_p20/20151203_233059_00_Video.avi |
|p21  |s11/part2_layout_p21/20151208_202507_00_Video.avi |
|p22  |s11/part1_layout_p22/20151208_200654_00_Video.avi |
|p23  |s12/part2_layout_p23/20151209_173604_00_Video.avi |
|p24  |s12/part1_layout_p24/20151209_171744_00_Video.avi |
|p27  |s14/part2_layout_p27/20151210_184405_00_Video.avi |
|p28  |s14/part1_layout_p28/20151210_181410_00_Video.avi |
|p29  |s15/part2_layout_p29/20151217_022713_00_Video.avi |
|p30  |s15/part1_layout_p30/20151217_021516_00_Video.avi |
|p33  |s17/part2_layouts_p33/20160128_195448_00_Video.avi|
|p34  |s17/part1_layouts_p34/20160128_194418_00_Video.avi|
|p37  |s19/part2_layouts_p37/20160202_005824_00_Video.avi|
|p38  |s19/part1_layouts_p38/20160202_004632_00_Video.avi|
|p41  |s21/part2_layout_p41/20160205_194405_00_Video.avi |
|p42  |s21/part1_layout_p42/20160205_191454_00_Video.avi |

## Speech and Gesture AMR (ELAN)

This folder contains the speech and gesture AMR annotations. Files can be opened in [ELAN](https://archive.mpi.nl/tla/elan). Filenames are labeled either by annotator (a1 through a5), or with "gold" for the gold standard. Each file contains the following five tiers of annotations:

- Speech
  - Transcripts created using [Coqui STT](https://github.com/coqui-ai/STT) and manually corrected
- Speech AMR
  - Speech AMRs created by our annotators
- Gesture - Label
  - Physical gesture labels from EGGNOG
- Gesture - Intent
  - Gesture intent labels from EGGNOG
- Gesture AMR
  - Gesture AMRs created by our annotators

## Multi-sentence AMR (Anafora)

This folder contains the multi-sentence AMR annotations, created using [Anafora](https://github.com/weitechen/anafora). If using Anafora, place the contents of this folder (.schema, MultimodalAMRAnnotationProject, and .setting.xml) in the "project file". Alternatively, since the annotations are XML files, they can be opened in a standard text editor. Filenames have the form [label].Medicine.[annotator or gold].completed.xml. Files contain the following types of annotations:

- Entities
  - EntitySuggestion
  - EventSuggestion
  - PossibleImplicit
- Relations
  - IdentityChain
  - SetMember
  - PartWhole

"Entities" were automatically generated using the MS-AMR toolkit, while "Relations" were created by our annotators.

## Contact

Please contact Kenneth Lai (klai12@brandeis.edu) if you have any questions!
