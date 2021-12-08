
# DNA Sequencing

Parallel and Distributed computing is the future of technology. All products and their fundamental concepts are being shifted to a parallel computing model. Everybody would agree that serial computing is easy to implement and use, but simply not efficient enough for industry-level purposes. Due to this reason, day by day a higher number of industries are providing and using cloud solutions which work on the basis of parallel and distributed computing. Eventually everything will be based on parallel and distributed computing and we wanna make out contribution towards it by parallelization of important algorithms such as the sequence alignment and finding hidden states algorithm.
Sequence alignment is the process of comparing and detecting similarities between biological sequences. What “similarities” are being detected will depend on the goals of the particular alignment process. Sequence alignment appears to be extremely useful in a number of bioinformatics applications. It is basically of two types: the global sequence alignment and the local sequence alignment. In global alignment, we find the superior counterpart between parts of the sequences. On the other hand, local alignment algorithms try to match parts of sequences and not the entirety of them. Local alignment is faster than global alignment, due to the lack of need to align the entire sequences.

## Description
Sequence Alignment or sequence comparison lies at heart of the bioinformatics, which describes the way of arrangement of DNA/RNA or protein sequences, in order to identify the regions of similarity among them. It is used to infer structural, functional and evolutionary relationship between the sequences. Alignment finds similarity level between query sequence and different database sequences. The algorithm works by dynamic programming approach which divides the problem into smaller independent sub problems. It finds the alignment more quantitatively by assigning scores. There are two types of algorithms which can solve the problem:-
- **Smith Waterman -** The Smith–Waterman algorithm performs local sequence alignment; that is, for determining similar regions between two strings of nucleic acid sequences or protein sequences. Instead of looking at the entire sequence, the Smith–Waterman algorithm compares segments of all possible lengths and optimizes the similarity measure. The algorithm was first proposed by Temple F. Smith and Michael S. Waterman in 1981. Like the Needleman–Wunsch algorithm, of which it is a variation, Smith–Waterman is a dynamic programming algorithm. As such, it has the desirable property that it is guaranteed to find the optimal local alignment with respect to the scoring system being used (which includes the substitution matrix and the gap-scoring scheme). The main difference to the Needleman–Wunsch algorithm is that negative scoring matrix cells are set to zero, which renders the (thus positively scoring) local alignments visible. Traceback procedure starts at the highest scoring matrix cell and proceeds until a cell with score zero is encountered, yielding the highest scoring local alignment. Because of its quadratic complexity in time and space, it often cannot be practically applied to large-scale problems.

- **Viterbi -** The Viterbi algorithm is a dynamic programming algorithm for obtaining the maximum a posteriori probability estimates of the most likely sequence of hidden states—called the Viterbi path—that results in a sequence of observed events, especially in the context of Markov information sources and hidden Markov models (HMM). The Viterbi algorithm is named after Andrew Viterbi, who proposed it in 1967 as a decoding algorithm for convolutional codes over noisy digital communication links. It has, however, a history of multiple invention, with at least seven independent discoveries, including those by Viterbi, Needleman and Wunsch, and Wagner and Fischer. It was introduced to Natural Language Processing as a method of part-of-speech tagging as early as 1987. Viterbi path and Viterbi algorithm have become standard terms for the application of dynamic programming algorithms to maximization problems involving probabilities. For example, in statistical parsing a dynamic programming algorithm can be used to discover the single most likely context-free derivation (parse) of a string, which is commonly called the "Viterbi parse". Another application is in target tracking, where the track is computed that assigns a maximum likelihood to a sequence of observations. 


## Run Locally

Clone the project
```bash
  git clone https://github.com/ayan2809/DNA-Sequencing.git
```

Go to the project directory

```bash
  cd DNA-Sequencing
```

Go to the smith-waterman directory

```bash
  cd smith-waterman
```

Compile Smith-Waterman serial code
```bash
  gcc -fopenmp smith_waterman_serial.c -o waterman_serial -lm 
```

Compile Smith-Waterman parallel code
```bash
  gcc -fopenmp smith_waterman_parallel.c -o waterman_parallel -lm 
```

Check the Time in seconds
```bash
  time ./waterman_serial
  time ./waterman_parallel
```

Go to the Viterbi directory

```bash
  cd smith-waterman
```

Compile Viterbi serial code
```bash
  gcc -fopenmp viterbi_serial.c -o viterbi_serial -lm 
```

Compile Viterbi parallel code
```bash
  gcc -fopenmp viterbi_parallel.c -o viterbi_parallel -lm 
```

Check the Time in seconds
```bash
  time ./viterbi_serial
  time ./viterbi_parallel
```


## Code Outputs

### Smith Waterman
<p align="center">
  <img src=https://user-images.githubusercontent.com/63350417/145221371-cab696de-b217-4542-a223-5d814e045f99.png>
            <br>
         <img src=https://user-images.githubusercontent.com/63350417/145221491-5d743736-1cf0-4243-a013-f374b1fd4e1a.png> 
  </p>


### Viterbi
<p align="center">
  <img src=https://user-images.githubusercontent.com/42286904/145219780-e6abc18a-f2b0-489a-a82a-16313bbb9f1a.png>
  <br>
  <img src=https://user-images.githubusercontent.com/42286904/145219798-38aef4d2-f36c-4b35-a284-66a7e52daa20.png>
 </p>




## Tech Stack Used

C, OpenMP parallel programming

## Authors

- [Aniket Bansal](https://github.com/nicolausmaximus)
- [Ayan Sadhukhan](https://github.com/ayan2809)
- [Dhruv Patel](https://github.com/)


