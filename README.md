# HSBMAS - Hierarchical Switching-Backbone Multi-agent System

## 1. Introduction
It is well known that network topology plays a key role in the convergence theory of multi-agent systems, a sufficient condition for convergence is that the topology be sufficiently well connected over periodic windows of time [<sup>[1]</sup>](#refer-problem). Consider a traditional peer-to-peer multi-agent architecture where each agent communicates directly with all other perceived neighbors based on Select-All-Neighbors (*SAN*), each agent needs to select all neighbors in a communication region to update its own state using the consensus algorithm (1). However, the evolution of each agent is computationally infeasible when the number of neighbors increases exponentially and, the multi-agent system is prone to split into multiple clusters when the distribution of agents are irregular. 

<div align=center>
    <img src="https://github.com/kyoran/HSBMAS/blob/main/img/protocol.png" width="40%" alt="consensus protocol" >
</div>

<div align=right>
    <b>(1)</b>
</div>

HSBMAS is a fully decentralized framework of the multi-agent system for consensus seeking. The framework can control the convergence evolution with hierarchical features of the network topology by only referring to local one-hop and two-hop neighbors' state. Notably, the proposed framework runs in a distributed and synchronous fashion. The diagram of our framework is shown as

<div align=center>
    <img src="https://github.com/kyoran/HSBMAS/blob/main/example/diagram.gif" width="40%">
    <img src="https://github.com/kyoran/HSBMAS/blob/main/example/framework.png" 
        alt="framework"/>
    <br>
    <b>Fig 1. Illustration of the proposed framework</b>
</div>

## 2. Dataset 
This project contains the dataset of 10 types of topological structures in the square <i>20r<sub>c</sub> × 20r<sub>c</sub></i> and, each of which has five different densities described as <i>ρ=N/L<sup>2</sup></i> and is connected initially. The density *ρ* represents that *N* agents distributed in a square-shape area of linear size *L* [<sup>[2]</sup>](#refer-density). A total of 50 topologies with different densities (*ρ≈2,4,6,8,10*) and different types are used for interesting and fair comparisons across proposed architecture *HSBMAS* and traditional architecture *SAN*. The naming format of these topologies is: *Type-N*.

- ***Uniform-N***: *N* agents are uniformly distributed over the semi open closed interval *[-4, 4)*.
- ***Ring-N***: *N* agents are randomly distributed on the ring with radius of *4*.
- ***Vase-N***:  *N* agents are randomly distributed on the curve of Vase which is formed according to [<sup>[3]</sup>](#refer-vase).
- ***Taiji-N***: *N-30* agents are uniformly distributed on the curve of Taiji. Besides, a vertical line composed of *30* agents is added to the center of Taiji to ensure initial connectivity.
- ***Circle-N***: *N* agents are randomly distributed in the circle with radius of *4*.
- ***Triangle-N***: *N* agents are randomly distributed in equilateral triangle with side length *9*.
- ***Square-N***: *N* agents are randomly distributed in four concentric squares centered at the origin, the length of their sides from outside to inside are 1.6, 1.12, 0.64 and 0.16, respectively.
- ***Arch-N***: *0.34N* and *0.63N* agents are randomly distributed on the curve of left and right 'archimedean spiral antenna' (abbr. 'Arch') respectively, and *0.03N* agents are designed to connect two Archs. (Inspired by [<sup>[4]</sup>](#refer-vase))
- ***Neat square-N***: It is a neat topology generated by dividing a circle into 20 equal parts and placing an agent at equal radian intervals.
- ***Neat radiation-N***: There are *N* agents neatly placed in a square area, the longitudinal and lateral gaps between nearest two agents are same.

The statistics of these initial topologies with varying densities are shown in Table I which contains the number of edges of adjacency matrix (i.e. #A-edges).

<div align="center">
    <b>Table I. The statistics of designed topologies in the same range <i>L = 20r<sub>c</sub></i></b>
    <table border="1">
      <tr>
        <th align="center">#A-edges</th>
        <th align="center">ρ≈2</th>
        <th align="center">ρ≈4</th>
        <th align="center">ρ≈6</th>
        <th align="center">ρ≈8</th>
        <th align="center">ρ≈10</th>
      </tr>
      <tr>
        <td align="center">Uniform</td>
        <td align="center">200</td>
        <td align="center">684</td>
        <td align="center">2118</td>
        <td align="center">3387</td>
        <td align="center">5848</td>
      </tr>
      <tr>
        <td align="center">Ring</td>
        <td align="center">549</td>
        <td align="center">1562</td>
        <td align="center">4484</td>
        <td align="center">8329</td>
        <td align="center">13036</td>
      </tr>
      <tr>
        <td align="center">Vase</td>
        <td align="center">744</td>
        <td align="center">3650</td>
        <td align="center">7669</td>
        <td align="center">13998</td>
        <td align="center">21441</td>
      </tr>
      <tr>
        <td align="center">Taiji</td>
        <td align="center">667</td>
        <td align="center">2054</td>
        <td align="center">4849</td>
        <td align="center">8654</td>
        <td align="center">14036</td>
      </tr>
      <tr>
        <td align="center">Circle</td>
        <td align="center">267</td>
        <td align="center">1141</td>
        <td align="center">2693</td>
        <td align="center">4670</td>
        <td align="center">7419</td>
      </tr>
      <tr>
        <td align="center">Triangle</td>
        <td align="center">278</td>
        <td align="center">1603</td>
        <td align="center">3721</td>
        <td align="center">6298</td>
        <td align="center">10195</td>
      </tr>
      <tr>
        <td align="center">Square</td>
        <td align="center">272</td>
        <td align="center">1120</td>
        <td align="center">2867</td>
        <td align="center">4990</td>
        <td align="center">7985</td>
      </tr>
      <tr>
        <td align="center">Arch</td>
        <td align="center">486</td>
        <td align="center">1921</td>
        <td align="center">4705</td>
        <td align="center">8271</td>
        <td align="center">13044</td>
      </tr>
      <tr>
        <td align="center">Neat square</td>
        <td align="center">420</td>
        <td align="center">840</td>
        <td align="center">1200</td>
        <td align="center">1624</td>
        <td align="center">3906</td>
      </tr>
      <tr>
        <td align="center">Neat radiation</td>
        <td align="center">890</td>
        <td align="center">2440</td>
        <td align="center">5040</td>
        <td align="center">8610</td>
        <td align="center">13190</td>
      </tr>
    </table>
</div>

## 2.1 ρ≈2
<div align="center">
    <table>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/001log_uniform_200/init_1_hop_conn.png" /><br><b><i>Uniform-200</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/002log_ring_200/init_1_hop_conn.png" /><br><b><i>Ring-200</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/003log_vase_200/init_1_hop_conn.png" /><br><b><i>Vase-200</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/004log_taiji_200/init_1_hop_conn.png" /><br><b><i>Taiji-200</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/005log_circle_200/init_1_hop_conn.png" /><br><b><i>Circle-200</i></b></td>
        </tr>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/006log_triangle_200/init_1_hop_conn.png" /><br><b><i>Triangle-200</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/007log_square_200/init_1_hop_conn.png" /><br><b><i>Square-200</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/008log_arch_200/init_1_hop_conn.png" /><br><b><i>Arch-200</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/009log_neat_square_225/init_1_hop_conn.png" /><br><b><i>Neat square-225</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/010log_neat_radiation_200/init_1_hop_conn.png" /><br><b><i>Neat radiation-200</i></b></td>
        </tr>
    </table>
</div>

## 2.2 ρ≈4
<div align="center">
    <table>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/001log_uniform_400/init_1_hop_conn.png" /><br><b><i>Uniform-400</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/002log_ring_400/init_1_hop_conn.png" /><br><b><i>Ring-400</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/003log_vase_400/init_1_hop_conn.png" /><br><b><i>Vase-400</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/004log_taiji_400/init_1_hop_conn.png" /><br><b><i>Taiji-400</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/005log_circle_400/init_1_hop_conn.png" /><br><b><i>Circle-400</i></b></td>
        </tr>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/006log_triangle_400/init_1_hop_conn.png" /><br><b><i>Triangle-400</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/007log_square_400/init_1_hop_conn.png" /><br><b><i>Square-400</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/008log_arch_400/init_1_hop_conn.png" /><br><b><i>Arch-400</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/009log_neat_square_441/init_1_hop_conn.png" /><br><b><i>Neat square-441</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-400/010log_neat_radiation_400/init_1_hop_conn.png" /><br><b><i>Neat radiation-400</i></b></td>
        </tr>
    </table>
</div>

## 2.3 ρ≈6
<div align="center">
    <table>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/001log_uniform_600/init_1_hop_conn.png" /><br><b><i>Uniform-600</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/002log_ring_600/init_1_hop_conn.png" /><br><b><i>Ring-600</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/003log_vase_600/init_1_hop_conn.png" /><br><b><i>Vase-600</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/004log_taiji_600/init_1_hop_conn.png" /><br><b><i>Taiji-600</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/005log_circle_600/init_1_hop_conn.png" /><br><b><i>Circle-600</i></b></td>
        </tr>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/006log_triangle_600/init_1_hop_conn.png" /><br><b><i>Triangle-600</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/007log_square_600/init_1_hop_conn.png" /><br><b><i>Square-600</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/008log_arch_600/init_1_hop_conn.png" /><br><b><i>Arch-600</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/009log_neat_square_625/init_1_hop_conn.png" /><br><b><i>Neat square-625</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-600/010log_neat_radiation_600/init_1_hop_conn.png" /><br><b><i>Neat radiation-600</i></b></td>
        </tr>
    </table>
</div>

## 2.4 ρ≈8
<div align="center">
    <table>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/001log_uniform_800/init_1_hop_conn.png" /><br><b><i>Uniform-800</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/002log_ring_800/init_1_hop_conn.png" /><br><b><i>Ring-800</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/003log_vase_800/init_1_hop_conn.png" /><br><b><i>Vase-800</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/004log_taiji_800/init_1_hop_conn.png" /><br><b><i>Taiji-800</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/005log_circle_800/init_1_hop_conn.png" /><br><b><i>Circle-800</i></b></td>
        </tr>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/006log_triangle_800/init_1_hop_conn.png" /><br><b><i>Triangle-800</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/007log_square_800/init_1_hop_conn.png" /><br><b><i>Square-800</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/008log_arch_800/init_1_hop_conn.png" /><br><b><i>Arch-800</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/009log_neat_square_841/init_1_hop_conn.png" /><br><b><i>Neat square-841</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-800/010log_neat_radiation_800/init_1_hop_conn.png" /><br><b><i>Neat radiation-800</i></b></td>
        </tr>
    </table>
</div>

## 2.5 ρ≈10
<div align="center">
    <table>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/001log_uniform_1000/init_1_hop_conn.png" /><br><b><i>Uniform-1000</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/002log_ring_1000/init_1_hop_conn.png" /><br><b><i>Ring-1000</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/003log_vase_1000/init_1_hop_conn.png" /><br><b><i>Vase-1000</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/004log_taiji_1000/init_1_hop_conn.png" /><br><b><i>Taiji-1000</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/005log_circle_1000/init_1_hop_conn.png" /><br><b><i>Circle-1000</i></b></td>
        </tr>
        <tr>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/006log_triangle_1000/init_1_hop_conn.png" /><br><b><i>Triangle-1000</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/007log_square_1000/init_1_hop_conn.png" /><br><b><i>Square-1000</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/008log_arch_1000/init_1_hop_conn.png" /><br><b><i>Arch-1000</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/009log_neat_square_1024/init_1_hop_conn.png" /><br><b><i>Neat square-1024</i></b></td>
            <td align="center"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-1000/010log_neat_radiation_1000/init_1_hop_conn.png" /><br><b><i>Neat radiation-1000</i></b></td>
        </tr>
    </table>
</div>

# Reference

<div id="refer-problem"></div>

- [1] [Nedić A, Olshevsky A, Rabbat M G. Network topology and communication-computation tradeoffs in decentralized optimization[J]. Proceedings of the IEEE, 2018, 106(5): 953-976.](https://ieeexplore.ieee.org/abstract/document/8340193/)

<div id="refer-density"></div>

- [2] [Vicsek T, Czirók A, Ben-Jacob E, et al. Novel type of phase transition in a system of self-driven particles[J]. Physical review letters, 1995, 75(6): 1226-1229.](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.75.1226)

<div id="refer-vase"></div>

- [3] [Dongdong Zha, Di Zhang, Huayong Liu. Construction of smooth blending of three-parameter curves and optimization of parameters[J]. Journal of Graphics, 2020, 41(05): 725-732. (in Chinese)](https://kns.cnki.net/kcms/detail/detail.aspx?dbcode=CJFD&dbname=CJFDLAST2020&filename=GCTX202005005&v=UNJTcmu%25mmd2BCFna5ViMyp0VX%25mmd2BP8ViKBRwbuzbliscRaPK0Lo6zgD9jJ1k4xv7RAShXX)

<div id="refer-arch"></div>

- [4] [Kaiser J. The Archimedean two-wire spiral antenna[J]. IRE Transactions on Antennas and Propagation, 1960, 8(3): 312-323.](https://ieeexplore.ieee.org/abstract/document/1144840)
