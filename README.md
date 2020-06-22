## Multi-paradigm modelling modelling in Python

The [PTTI software package] is designed for running epidemiological models
with interventions. It contains the models used in our technical 
[SEIR-TTI paper] where we show how to do testing and contact tracing in
a compartmental model and our more policy-oriented [PTTI paper] where
we use it to explore a number of policy scenarios for the UK. The
software is

  * Formalism-agnostic: we believe in checking models against each other,
    as it's the best way to understand which models work best in what 
    circumstances. So we have ordinary differential equation models,
    agent-based models, network, and rule-based models.
  * Simple configuration: simulations are described in a user-friendly
    YAML file (though there is nothing to prevent running them directly
    in [Python] if you wish).
  * Interventions: the simulation is stopped at set times or on certain
    conditions, parameters are changed, and the simulation continues.
  * Parallel execution: simulations can be conducted in parallel using
    as many CPUs as are available, and also supports [MPI] for use in
    High-Performance Computing environments.
  * Easy extension to other models: we provide an interface definition
    that any model implementation with any number of compartments or 
    states or agents can use to be incorporated into the simulation
    machinery. It does have to be written in [Python]. We're sorry, it
    would have taken too long to make this software in [Haskell].
  
## Scaling up epidemiological models with RBM

This is a collection of models as described in our paper,
[Scaling up epidemiological models with rule-based modelling].
They are written in the [Kappa language] and the models themselves
can be found in the [models/ subdirectory] of the repository on
the Github. It is also possible to simulate them in your
[web browser] with the links below:

* [Masks]
* [Fomites and hand-washing]
* [Vector-borne disease]
* [Testing]
* [Testing and contact tracing]
* [Schools as accelerants]
* [Gathering and superspreading]

[PTTI software package]: https://github.com/ptti/ptti
[SEIR-TTI paper]: https://github.com/ptti/ptti/raw/master/docs/tti.pdf
[PTTI paper]: https://github.com/ptti/ptti/raw/master/docs/PTTI-Covid-19-UK.pdf
[rule-based models]: http://kappalanguage.org/
[Python]: https://python.org/
[MPI]: https://www.mpi-forum.org/
[Haskell]: https://www.haskell.org/
[Masks]: https://ptti.github.io/kasim/?model=https%3A//raw.githubusercontent.com/ptti/rule-based-models/master/models/masks.ka
[Fomites and hand-washing]: https://ptti.github.io/kasim/?model=https%3A//raw.githubusercontent.com/ptti/rule-based-models/master/models/fomites.ka
[Vector-borne disease]: https://ptti.github.io/kasim/?model=https%3A//raw.githubusercontent.com/ptti/rule-based-models/master/models/mosquitoes.ka
[Testing]: https://ptti.github.io/kasim/?model=https%3A//raw.githubusercontent.com/ptti/rule-based-models/master/models/testing.ka
[Testing and contact tracing]: https://ptti.github.io/kasim/?model=https%3A//raw.githubusercontent.com/ptti/rule-based-models/master/models/tracing.ka
[Schools as accelerants]: https://ptti.github.io/kasim/?model=https%3A//raw.githubusercontent.com/ptti/rule-based-models/master/models/school.ka
[Gathering and superspreading]: https://ptti.github.io/kasim/?model=https%3A//raw.githubusercontent.com/ptti/rule-based-models/master/models/super.ka
[Kappa language]: https://kappalanguage.org/
[models/ subdirectory]: https://github.com/ptti/rule-based-models/tree/master/models
[web browser]: https://ptti.github.com/kasim/
