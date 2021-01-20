# FunctionalObservability
Functional observability analysis, minimum sensor placement and minimum-order functional observer design on large-scale dynamical networks, including applications to power grids and epidemics.

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

The full text of the GNU General Public License can be found in the file "LICENSE.txt".

# Dependency
For the cyber-attack detection problem in power grids (example_cyberdetection), Matpower 6.0 (https://matpower.org/download/) is required for the power flow calculation.

# Usage
find_msp : Finds the minimum set of sensor nodes required for the system functional observability with respect to a set of target nodes. This is a MATLAB implementation of Algorithm 1 in Ref. [1].

find_F0 : Finds F_0 with minimum-order such that Darouach's condition (4) in Ref. [1] is satisfied for a triple (A,C,F_0). This is a MATLAB implementation of Algorithm 2 in Ref. [1].

functobsv_design : Designs the functional observer's matrices (N,J,H,D,E) in Eq. (9) in Ref. [1]. The design method, originally proposed in Ref. [2], is guaranteed to provide a stable functional observer if the triple (A,C,F0) satisfies Darouach's conditions (4-5) in Ref. [1]. This code provides a MATLAB implementation of Algorithm 3.5.1 in Ref. [3].

example_dynamicalnetwork : Example of minimum sensor placement and minimum-order functional observer design for a random complex dynamical networks. This code examplifies how to:
    (1) apply Algorithm 1 to determine the minimum set of sensor nodes for functional observability of a dynamical network with respecto to a given set of target nodes; and
    (2) apply Algorithm 2 to design a minimum-order functional observer.
Both algorithms are further described in Ref. [1] and codes "find_msp.m" and "find_F0.m".

example_cyberdetection : Example of cyber-attack detection in power grids using functional observers and target state estimation.

example_epidemicspreading : Example of sensor placement and observer design for target state estimation in epidemics.

