# HSBMAS - Hierarchical Switching-Backbone Multi-agent System
<style>
    td {text-align:"center", valign="middle"}
</style>
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

## 2.1 ρ≈2
<div align="center">
    <table styple="text-align:center;margin:0 auto;border:0">
        <tr>
            <td align="center" valign="middle"><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/001log_uniform_200/init_1_hop_conn.png" /><br><b><i>Uniform-200</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/002log_ring_200/init_1_hop_conn.png" /><br><b><i>Ring-200</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/003log_vase_200/init_1_hop_conn.png" /><br><b><i>Vase-200</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/004log_taiji_200/init_1_hop_conn.png" /><br><b><i>Taiji-200</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/005log_circle_200/init_1_hop_conn.png" /><br><b><i>Circle-200</i></b></td>
        </tr>
        <tr>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/006log_triangle_200/init_1_hop_conn.png" /><br><b><i>Triangle-200</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/007log_square_200/init_1_hop_conn.png" /><br><b><i>Square-200</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/008log_arch_200/init_1_hop_conn.png" /><br><b><i>Arch-200</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/009log_neat_square_225/init_1_hop_conn.png" /><br><b><i>Neat square-225</i></b></td>
            <td><img src="https://github.com/kyoran/HSBMAS/blob/main/Agents-200/010log_neat_radiation_200/init_1_hop_conn.png" /><br><b><i>Neat radiation-200</i></b></td>
        </tr>
    </table>
</div>

## 2.2 ρ≈4
<div align=center>
    
</div>

## 2.3 ρ≈6
<div align=center>
    
</div>

## 2.4 ρ≈8
<div align=center>
    
</div>

## 2.5 ρ≈10
<div align=center>
    
</div>

# Reference
<div id="refer-topology"></div>

- [1] [Vicsek T, Czirók A, Ben-Jacob E, et al. Novel type of phase transition in a system of self-driven particles[J]. Physical review letters, 1995, 75(6): 1226.](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.75.1226)
