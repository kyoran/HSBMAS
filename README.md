# HSBMAS - Hierarchical Switching-Backbone Multi-agent System

## 1. Introduction
HSBMAS is a fully decentralized framework of the multi-agent system for consensus seeking. The framework can control the convergence evolution with hierarchical features of the network topology by only referring to local one-hop and two-hop neighbors' state. Notably, the proposed framework runs in a distributed and synchronous fashion. The diagram of our framework are shown in the following figures.

<div align=center>
    <img src="https://github.com/kyoran/HSBMAS/blob/main/example/diagram.gif" width="40%">
    <img src="https://github.com/kyoran/HSBMAS/blob/main/example/framework.png" 
        alt="framework"/>
    <br>
    <b>Fig 1. Illustration of the proposed framework</b>
</div>

## 2. Dataset 
This project contains the dataset of 10 types of topological structures in the square <i>20r<sub>c</sub> × 20r<sub>c</sub></i> and, each of which has five different densities described as <i>ρ=N/L<sup>2</sup></i> and is connected initially. The density *ρ* represents that *N* agents distributed in a square-shape area of linear size *L* [<sup>[1]</sup>](#refer-topology). A total of 50 topologies (*ρ≈2,4,6,8,10*) are used for interesting and fair comparisons across proposed architecture *HSBMAS* and traditional architecture *SAN*. The naming format of these topologies is: *Type-N*.

<b><i>Uniform-200</i></b>: *N* agents are uniformly distributed over the semi open closed interval *[-4, 4)*.

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
<div id="refer-topology"></div>

- [1] [Vicsek T, Czirók A, Ben-Jacob E, et al. Novel type of phase transition in a system of self-driven particles[J]. Physical review letters, 1995, 75(6): 1226.](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.75.1226)
