# Using Julia to build the simulation pipeline of an astronomical instrument
## Maurizio Tomasi (Università degli Studi di Milano)


In this short talk I will describe the way we used Julia to develop the simulation pipeline for the LSPE/Strip instrument, a microwave polarimeter that will be used to measure the signal of the Galaxy in the frequency bands 40–90 GHz from ground. As the pipeline needs to simulate and per-process a huge amount of non-chunkable data (~1 TB), we picked Julia because of its promise of being efficient as C++ and Fortran. We avoided using a mixture of Python, C++, and Fortran as we used to do, because this usually prevents young researchers with no proper background in computer science from hacking and contributing to these code-bases. Moreover, we were intrigued by Julia's interactivity through the REPL, IJulia, and Pluto. My team loved the language and was able to be productive and produce reasonably efficient code; moreover, the interactivity permitted to quickly test ideas, and the package system eased the deployment of the pipeline to HPC clusters. On the other hand, at times we experienced bottlenecks in the code because people were not able to write «good» code at their first attempt as they did with more standard languages like C++ and Fortran. Moreover, sometimes the lack of good libraries hampered the development every now and then: as an example, to ease the deployment of the pipeline the author had to develop a Healpix pixelization library in Julia from scratch!