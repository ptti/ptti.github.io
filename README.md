## Computational models for Population-wide Testing, Tracing and Isolation

### Multi-paradigm modelling environment in Python

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
  
[PTTI software package]: https://github.com/ptti/ptti
[SEIR-TTI paper]: https://github.com/ptti/ptti/raw/master/docs/tti.pdf
[PTTI paper]: https://github.com/ptti/ptti/raw/master/docs/PTTI-Covid-19-UK.pdf
[rule-based models]: http://kappalanguage.org/
[Python]: https://python.org/
[MPI]: https://www.mpi-forum.org/
[Haskell]: https://www.haskell.org/
