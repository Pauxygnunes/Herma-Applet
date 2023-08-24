# Herma-Applet

The Herma Applet v 0.1 application was designed to illustrate part of the Formalized Music discipline, held at UFRJ Graduate Program in Music during the 2020-1 semester.

The application generates, from the instructions and maps provided by Iannis Xenakis, in chapter VI (Symbolic Music) of his book Formalized Music, renderings of possible versions of the piece Herma, for solo piano, which vary according to random drawings of three sets. (A, B and C), of their durations, attack points and dynamics.

Herma Applet has versions for Windows and Mac OS. To check the rendered MIDI files, you need to link in the system the file type (.mid) with a preferred program (DAW, score editor, or programming platform).

## Installation
Download and run the installation file corresponding to your system
- [Herma Applet Installer (Windows)](https://www.dropbox.com/scl/fo/2df6jpkus3lu50oasc6fr/h?rlkey=4gc8bgtcmhuqj6sqkoyivtyb8&dl=0)
- [Herma Applet Installer (Mac OS)](https://www.dropbox.com/scl/fo/xbmnwh6wbji7iye21ql0f/h?rlkey=j807l4oe6urgu3vbtjzjhzho0&dl=0)

## Interface Elements
Herma’s interface starts with the parameters of the original piece (planned by Xenakis) loaded. The two tables are called _hermadata_ and _notematrix_.

![hermaui](https://github.com/Pauxygnunes/Herma-Applet/assets/30673056/07cafd41-50f9-4612-be60-c93dd6ed8c77)


This does not mean that the program will render a version of Herma identical to the score, but only that the rendered file will have an overall shape similar to that expressed in the map on page 177 of the FM book – the duration of its sections with its rhythmic densities, and the combination of their sets. Sets themselves will be sorted from scratch, with random pitches and cardinalities.

User can edit tables freely, allowing experiments with rendering with other parameters.

## Buttons

- Reset – returns the tables to the default initial data, referring to the map on page 177, related to the Xenakis work.
- New MIDI – the program generates a brand new MIDI from the data entered in hermadata and notematrix tables. Each time the button is pressed, a new version will be generated, always following the restrictions defined by the tables. The rendered file will open automatically by the program defined in the system to handle Midi files.
- Save – saves the hermadata file as a *.mat file for later use.
- Load – loads *.mat files previously saved by the program.

## Table

- **Hermadata** – each row corresponds to a module in the map on page 177. The columns define six categories of data, respectively:
1. Corresponding index to the piece section. Here, it is assumed that the piece is divided into four major sections – 1. Introduction with R; 2. Presentation of sets A, B and C and their complements; 3. Operations converging to ~A~BC, which corresponds to field 4 of pitches; 4. Operations converging to F, final group.
2. Corresponding index to the combination of pitch fields. Each one of the indices also corresponds to the Venn graphs exposed on pages 174, 176 and 177 of the book Formalized Music, by Iannis Xenakis (Figures 1 and 2). The list was numbered in the order of entry into the piece.
3. Dynamics, considering the following convention: pp=20; f=80; ff=100; fff = 120.
4. Module duration, in seconds. This measure was taken from the proportional map, presented on page 177.
5. Module start time point, in seconds.
6. Average density of notes, in values per second.
- **Note Matrix** – each line corresponds to a note, following the MIDI Toolbox model, by Eerola and Toivianien, which has seven columns:
1. Attack time point (note on);
2. Note duration in beats.
3. Channel (as the piece is for solo piano, there is only one channel).
4. MIDI pitches.
5. Dynamics (see Hermadata item 3).
6. Time points in seconds.
7. Note durations in seconds.

![Fields v02](https://github.com/Pauxygnunes/Herma-Applet/assets/30673056/d56930ea-9269-45ad-ae19-f2678077dfb3)

![Sections](https://github.com/Pauxygnunes/Herma-Applet/assets/30673056/370726d4-d78c-4abe-9b36-75b9c86f97bb)

Herma Applet was made with Matlab®. The source code is provided here, in the file hermauimac.m. The structure is simple and details can be checked in the bibliography below.

![Herma Applet Structure](https://github.com/Pauxygnunes/Herma-Applet/assets/30673056/4ece41f5-cd93-4ea5-b854-48dd9ed16b98)

## References

Agon, Carlos, Moreno Andreatta, Gérard Assayag, and Stéphan Schaub. “Formal Aspects of Iannis Xenakis' ‘Symbolic Music’: A Computer-Aided Exploration of Compositional Processes.” _Journal of New Music Research_. 32(2): 145-159. https://doi.org/10.1080/0929821042000310621.

Gentil-Nunes, Pauxy. _Herma Applet_. V. 0.1 Alpha. PPGM-UFRJ. 2022. 

Gentil-Nunes, Pauxy; Simões, Luan; Viana, Petrucio. 2022. An Attempt at Extending Xenakis’ Compositional Design of Herma through Computational Tools. Xenakis 22 Centenary International Symposium. _Proceedings…_ Atenas: University of Atenas.

Gibson, Benoît. “On Herma.” In: Nakipbekova, Alfia (ed.). _Exploring Xenakis: Performance, Practice, Philosophy_, 53-66, Vernon Press, 2019.

Grossmann, Daniel. _Iannis Xenakis — Music for Keyboard Instruments — Realized by Computer_. Compact Disc. NEOS 10707, 2008.

Montague, Eugene. _The Limits of Logic: Structure and Aesthetics in Xenakis’s Herma_. Master’s thesis, University of Massachusetts at Amherst, 1995.

Morris, Robert. _Composition with Pitch Classes: A Theory of Compositional Design_. New Haven: Yale University, 1987.

Simões, Luan. _Hermoser_. V. 1.0. GitHub. 2022. https://github.com/luansimoes/Hermoser

Squibbs, R. “Musical composition as applied mathematics: set theory and probability in Iannis Xenakis’s ‘Herma’.” Bridges: Mathematical Connections in Art, Music, and Science. _Conference Proceedings_, 2000.

Straus, Joseph. _A Primer for Atonal Set Theory_. New York: CUNY, 1991. https://academicworks.cuny.edu/cgi/viewcontent.cgi?article=1473&context=gc_pubs.

Varga, Bálint András.1996. _Conversations with Iannis Xenakis_. Queen Square London: Faber and Faber.

Wannamaker, Robert. “Structure and Perception in Herma by Iannis Xenakis.” _Music Theory Online_ 7.3, 2001.

Xenakis, Iannis. _Herma_. Piano solo. Score. London: Boosey & Hawkes, 1967.

Xenakis, Iannis. 1992. _Formalized Music_. Stuyvesant NY: Pendragon Press.

==========

Copyright ©2021, Pauxy Gentil Nunes Filho (UFRJ), Luan Simões (UFRJ) and Petrucio Vianna (UFF)

[PArtiMus Research Group](https://partimus.art/)

[PPGM-UFRJ](https://ppgm.musica.ufrj.br/)


