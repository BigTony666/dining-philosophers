<h1 align="center">
    <img src="https://img.icons8.com/ios/100/000000/socrates.png">
    <br>
    <strong>Dining Philosophers</strong>
</h1>

<div align="center">
  <p>An implementation to solve Dining Philosophers Problem in Chandy/Misra algorithm by using pthreads.</p>
</div>

- [Implementation](#implementation)
- [How to run](#how-to-run)
- [OpenMP](#openmp)
- [Reference](#reference)

## Implementation

Chandy/Misra algorithm allows any number of philosophers(threads) to request for any number of forks(resources). At the beginning, for each philosopher who will compete for a resource, we initialize the forks and give each of them to the lower-ranking philosopher. Each fork is either clean or dirty. Initially, all the forks ate dirty. When a philosopher wants to use resources (that is, to eat), he must get it from his neighbors who compete with him. He sends a request for each fork that he currently does not have. When the philosopher who owns that fork receives the request from other philosopher, if the fork is clean, then he keeps it, otherwise it wipes it to clean and hand over the fork to that philosopher who requests it. When a philosopher finishes to eat, both his forks become dirty. If another philosopher had previously requested the fork, he wiped it clean and handed it over. This solution allows for a lot of parallelism and is suitable for arbitrary number of threads and resources. 
 
## How to run

Make sure the system has a `cmake` with a 2.8 or higher version, `gcc` with a 4.8 or higher version.

Run the cmake to generate makefile:

```sh
$ cmake .
```

Makefile has been created, just run `make` command in terminal:

```sh
$ make
```

An executable program called `philosophers_dinning` is generated.

Then you can run it and there is a CLI for the program:

```sh
$ ./philosophers_dinning

A CLI to visualize Philosophers Dinning Problem
Usage:
  ./philosophers_dinning [OPTION...]

  -n, --num arg  number of philosophers
      --help     Print help

```

Run the program with the specific argument:

```sh
$ ./philosophers_dinning -n 5
```

## OpenMP

In **openmp** directory, there is a OpenMP version of philosophers dinning solution. Make sure your compiler is supported OpenMP.

## Reference

[Dining philosophers problem](https://en.wikipedia.org/wiki/Dining_philosophers_problem)

 <a href="https://icons8.com/icon/39887/socrates" style="display:none;">Socrates icon by Icons8</a>
