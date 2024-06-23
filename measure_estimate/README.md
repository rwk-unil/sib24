# Measure and estimate your energy impact

# Activity M1 - Explore Electricity Maps

Visit the Electricity Maps website https://www.electricitymaps.com and open the App.

## Quests

* Can you find the country that currenlty has the lowest carbon intensity for power consumption ?
  <details>
  <summary>Solution</summary>
  This really depends, but usually France has a quite low carbon intensity thanks to their nuclear infrastructure. Nordic countries, and Switzerland don't do bad, they have a lot of hydro energy.
  </details>
* What about the highest carbon intensity for power production ?
  <details>
  <summary>Solution</summary>
  Some countries reach almost 1kgCO2/kWh !
  </details>
* What are the reasons for these results ?
  <details>
  <summary>Solution</summary>
  Their energy is coal based, they burn a lot of coal and this generates massive quantities of CO2 !
  </details>
* Can you find the data sources they use ?
  <details>
  <summary>Solution</summary>
  Search for their "applied methodologies" and read their "Data sources" description. The sources are documented on their GitHub <a href="https://github.com/electricitymaps/electricitymaps-contrib/blob/master/DATA_SOURCES.md">https://github.com/electricitymaps/electricitymaps-contrib/blob/master/DATA_SOURCES.md</a>
  </details>
* What about missing data, how do they estimate it ?
  <details>
  <summary>Solution</summary>
  <a href="https://www.electricitymaps.com/methodology#missing-data">https://www.electricitymaps.com/methodology#missing-data</a>
  </details>

# Activity M2 - Estimate your computation carbon footprint

Visit the Green-Algorithms website https://www.green-algorithms.org and open the calculator.

## Quests

* Try out several scenarios, can you make some that match your current bioinformatic workloads ?
  <details>
  <summary>Solution</summary>
  Tell me :)
  </details>
* Can you find your CPU ?
  <details>
  <summary>Solution</summary>
  I case you need to identify your CPU you can run "lscpu" on Linux based systems and it will show under "Model name:" e.g., "Model name:                         Intel(R) Xeon(R) Platinum 8124M CPU @ 3.00GHz"

  On MacOS the "About This Mac" tab only gives information like "Processor: 2.9 GHz Quad-Core Intel Core i7" which is not the exact model, through the command line you can find it with the following command "sysctl -a | grep cpu.brand" e.g., "machdep.cpu.brand_string: Intel(R) Core(TM) i7-6920HQ CPU @ 2.90GHz"

  On Windows you can right click "This PC" and click "Properties", the Processor model will be shown.
  </details>
* Not all CPU models are listed, did you know you can ask to add yours ?
  <details>
  <summary>Solution</summary>
  The data and code for the project is available on Github : <a href="https://github.com/GreenAlgorithms/green-algorithms-tool">https://github.com/GreenAlgorithms/green-algorithms-tool</a>
  The per CPU TDP (total dissipated power) is available in a CSV table : <a href="https://github.com/GreenAlgorithms/green-algorithms-tool/blob/master/data/latest/TDP_cpu.csv">https://github.com/GreenAlgorithms/green-algorithms-tool/blob/master/data/latest/TDP_cpu.csv</a>

  You can ask to add your CPU here : <a href="https://github.com/GreenAlgorithms/green-algorithms-tool/issues/1">https://github.com/GreenAlgorithms/green-algorithms-tool/issues/1</a>
  </details>
* How does your workload compare to a car ride or a Paris-London flight ?
  <details>
  <summary>Solution</summary>
  Was this what you expected ?
  </details>
* What is the formula that they use ? Can you adapt to light CPU loads ? e.g., tasks that consume only 50% of the CPU ?
  <details>
  <summary>Solution</summary>
  The formula: The carbon footprint is calculated by estimating the energy draw of the algorithm and the carbon intensity of producing this energy at a given location:

  carbon footprint = energy needed * carbon intensity

  Where the energy needed is:

  runtime * (power draw for cores * usage + power draw for memory) * PUE * PSF

  You can adapt the "usage" to 0.5 for 50% CPU usage.
  </details>
* Can you estimate the carbon emmisions for the variant calling on the 150,119 genomes in the UK Biobank ?
  If we take a look at their open-access paper : https://www.nature.com/articles/s41586-022-04965-x there is a section "Running time" in the methods section.
  > All jobs were run using 12 cores with 60 GB of reserved RAM. Approximately 1% of jobs were rerun using 24 cores with 120 GB reserved RAM. A few jobs requiring more cores and memory, with a single job finishing with 48 cores and 1,000 GB of RAM. Total reserved CPU time on cluster was 5.8 million CPU hours and total effective compute time of 5.0 million CPU hours. The difference in these numbers is explained by the fact that not all cores reserved for the program may not utilize all at the same time.
  <details>
  <summary>Solution</summary>
  Runtime : 5,000,000
  Type : CPU
  Number of cores : 12
  Model : Xeon Platinum 9282 (Probably not this exact model but likely a Xeon Platinum as I know they use them in their infrastructure)
  Memory available : 64 GB (they use 60 GB so let's have a bit more for the operating system)
  Cloud computing on Amazon Web Services (they use AWS)
  Location : Europe - United Kingdom (this data is so sensitive, it cannot move outside of the UK)

  Estimate :
  Carbon footprint : 151.21 Tons of CO2 ! 654.24 MWh ! 65.5 NYC-Melbourne flights

  Happily they don't have to rerun this everyday.
  </details>
* Massive right ? Can you guess the emissions for the 500,000 sample release ?
  <details>
  <summary>Solution</summary>
  We cannot simply multiply by 500/150, but it gives an estimate. The variant calling for the 500,000 dataset has much more variants roughly 1.2 trillion whereas the 150,119 has less than 600 million variants (cf. paper), and this also impacts runtime. We can probably guess that a 5-10x increase in energy and CO2 emissions is likely !
  </details>
