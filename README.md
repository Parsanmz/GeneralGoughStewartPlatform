# Gough-Stewart Platform FKP and IKP
FKP and IKP formulation and numerical solution of a Simple 6-DoF Gough-Stewart Platform

In this project, I am going to derive the Inverse and Forward Kinematics equations of the-so-called Gough-Stewart platform, which has 6 degrees-of-freedom. The platform is a parallel robot consisted of 6 linear actuators and two plates, as the base and end-effector. First, a closed-form inverse kinematics formulation will be suggested. Based on the IKP equations, a numerical solution will be performed on the robot to achieve an answer to the FKP. Afterwards, the jacobian matrix of the robot will be derived. **Note that everything will be verified here using MATLAB Simulink, so we will be sure that our models work. All the codes and simulations are done using MATLAB and MATLAB Simulink**

<p align="center">
  <img width="460" height="360" src="https://github.com/Parsanmz/GeneralGoughStewartPlatform/blob/main/GS.jpg">
</p>

The picture is from the book ["Parallel Robots"](https://aras.kntu.ac.ir/publications/parallel-robots-book/) by H. Taghirad

## Inverse Kinematics Problem (IKP)
In all of the notations, the term $P$ is the position of the end-effector, and the term $R$ is the rotation matrix. Let's note $R_1$ to be the radius of base, and $R_2$ to be the radius of the end-effector. As shown in the picture, the attach points on the base and end-effector are called $A_i$ and $B_i$ , respectively. The MSSM configuration of Gough-Stewart platforms happens where these attach points are placed by 60 degrees of distance through the circle. In this solution, the MSSM configuration is considered. Each actuator connects a point on the base to the end-effector, forming a kinematic chain. The kinematic chain for the $i_{th}$ actuator is shown as below: 
$$l_i^2=(P + R*b_i - a_i)(P + R*b_i - a_i)^T$$



