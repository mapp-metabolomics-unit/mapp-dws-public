---
id: m9c56hci1fztmro5jflwkcj
title: Molecular Networking
desc: ''
updated: 1726643229430
created: 1726643175364
---

To analyze the spectral diversity of the profile collection, a molecular network (MN) was created on the GNPS website (http://gnps.ucsd.edu) using the .mgf spectra file generated at the previous step (Wang et al., 2016). The precursor ion mass tolerance was set to 0.02 Da and an MS/MS fragment ion tolerance of 0.02 Da. A network was then created where edges were filtered to have a cosine score above 0.7 and more than six matched peaks. Further, edges between two nodes were kept in the network if and only if each of the nodes appeared in each other's respective top 10 most similar nodes. Finally, the maximum size of a spectral family was set to 100, and the lowest‐scoring edges were removed from molecular families until the molecular family size was below this threshold. The spectra in the network were then searched against GNPS spectral libraries. All matches kept between network spectra and library spectra were required to have a score above 0.7 and at least six matched peaks. The resulting MN is available online at https://gnps.ucsd.edu/ProteoSAFe/status.jsp?task=XXXXXXX. The converted mass spectrometry data files, the corresponding metadata table, and the metabolite annotation results table, together with a Cytoscape file corresponding to the full MN annotated with the experimental and theoretical spectral matches are available under the MassIVE ID MSVXXXXXXXX.