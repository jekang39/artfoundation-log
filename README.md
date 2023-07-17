# artfoundation-log
ARabidopsis Transcription regulatory Factor Domain-domain interaction based Analysis Tool- LLPS, Oligomerization, GO analysis

If you use ARTFOUNDATION-LOG, please cite the article below in your publication.
The article has been accepted for publication by the journal- "genes".
The final version will be updated soon in the prearchive server.

Kang, J.E.; Jun, J.H.; Kwon, J.H.; Lee, J.; Hwang, K.; Kim, S.; Jeong, N. ART FounDATion-LOG (ARabidopsis Transcription regulatory Factor Domain-domain interaction Analysis Tool-Liquid liquid phase separation, Oligomerization, Go analysis), a toolkit for interaction data based domain analysis. Preprints.org 2023, 2023060366. https://doi.org/10.20944/preprints202306.0366.v1

The program is for Linux/ Unix OS only. If you want to use in Windows, please change the codes accordingly. Sources are available in each program folder.

In download folder, three ARTFOUNDATION-LOG programs are available. Download any of the zip files available in download folder.
Select one that you want to download. Click the name and then you will go to the file page. Right-click "view raw" and select "save link" to download the file.

1.art_foundation_log_online: llps factors and their TF. You need to know how to program Java language to use this one. Otherwise, you can look at their outputs in output folder, if you are interested in details of outputs mentioned in the article.

2. artfoundation_log_arabido: you do not need to know how to program. 

2.1. open a terminal.
2.2. cd path_of_downloaded_file (e.g. cd /home/centos/artfoundation_log_arabido )
2.3. change the file "input_list" in the folder called "data". You can copy and paste your Arabidopsis thaliana gene list in the file: one gene per line.
2.4. copy and paste the following line.
java -cp .:lib/commons-io-2.11.0.jar:lib/commons-math3-3.6.1.jar:lib/commons-lang3-3.12.0.jar:lib/commons-collections4-4.4.jar:lib/commons-lang3-3.12.0.jar art_foundation_log_online_arabido >out_art_foundation_log_online_arabido_date_time

You will find your output files in output file folder. Output files are time-stamped in addition to time-stamped input_list file.

3. art_foundation_log_online_eukary: If you want to run the program for eukaryotic species other than Arabidopsis thaliana, you can use this one. However, outputs are from mainly three databases, ProtCAD, 3did, and DrLLPS. Although you do not need to know how to program, you need to provide a file that maps gene with Pfam assignment. Please look at the file "out_mix_interpro_genbank.final" in the folder, "data". You should provide one like it. Gene name should not contain space. And you need to give its file path in the line number 125 in the function called "map_pfam_to_eukary_gene". Once you complete creating the file and providing the path, all you need to do is to change the file "input_list" in the folder called "data". You can copy and paste your eukaryotic gene list in the file: one gene per line. The gene name should match with one in the pfam map file you provided.

3.1. open a terminal 
3.2. cd path_of_downloaded_file (e.g. cd /home/centos/art_foundation_log_online_eukary )
3.3. copy and paste the following line.
javac -nowarn -cp .:lib/commons-io-2.11.0.jar:lib/commons-math3-3.6.1.jar:lib/commons-lang3-3.12.0.jar:lib/commons-collections4-4.4.jar:lib/commons-lang3-3.12.0.jar art_foundation_log_online_eukary.java

Once it is successfully compiled, copy and paste the following line.
3.4. java -cp .:lib/commons-io-2.11.0.jar:lib/commons-math3-3.6.1.jar:lib/commons-lang3-3.12.0.jar:lib/commons-collections4-4.4.jar:lib/commons-lang3-3.12.0.jar art_foundation_log_online_eukary >out_art_foundation_log_online_eukary_date_time

You will find your output files in output file folder. Output files are saved with time-stamp in addition to time-stamped input_list file.


Last modified on July 5, 2023 


