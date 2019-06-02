Developed by Pavel A. Alvarez at West Autonomous University (Universidad Autónoma de Occidente) in Mexico.

**News:** H-electreIII 1.0 was released on Jun. 1, 2019.

**Notes:** If you use H-electreIII in your research or publish, please cite or acknowledge it.

> 

H-electreIII is the well-know ELECTRE III method, but extended for the multiple criteria hierarchy process (MCHP). It allow to aggregate the preference information and generate ranking of alternatives in any node of a hicerchy of criteria. 

For assistance and/or collaboration opportunities, please contact the author by mailing <pavel.alvarez@udo> or using the issue tracker on GitHub.


# hierarchy-ELECTREIII
The extended ELECTRE III method for the multiple criteria hierarchy process (MCHP).

How to run?
- ./H-ELECTRE-III-share <directory_with_input_files>
- ./H-ELECTRE-III-share my_project_name


## Description of the input and output data

> The input files shoul be saved in a directory inside the /projects

Example

projects/my_project_name

Running as
./H-ELECTRE-III-share my_project_name

## Input 

### direction.txt

> 0:minimization or 1 maximization

g_1

g_2

...

g_m


### hierarchy.txt

	        g
	      /    \
	     g1      g2
        /  \    /  \
      g11 g12  g21  g22
     /  \  |   / \  /  \
    c1 c2 c3  c4 c5 c6  c7
   

> The above hierarchy is represented with the follow format for the hierarchy.txt file


g={g1,g2}

g1={g11,g12}

g11 ={C1,c2}

c1

c2

g12={c3}

c3 

g2={g21, g22}

g21={ c4, C5}

c4 

c5 

g22={c6, C7}

c6 

c7 



### intercriteria.txt
> The space between data is tab [\t]

w_1 w_2 ... w_n

q_1 q_2 ... q_n

p_1 p_2 ... p_n

v_1 v_2 ... v_n



### performance.txt

g(a1_1) g(a1_2) ... g(a1_n)

g(a2_1) g(a2_2) ... g(a2_n)

...

g(am_1) g(am_2) ... g(am_n)


### problem.txt

4	'number of alternatives

3	'number of criteria



### use_veto.txt
-------------------------------
> specify if the criterion use veto factor 
> (0 do not use veto) or (1 use veto)

g_1

g_2

...

g_m



## Output 
- It is a valued outranking matrix and ranking for each node in the hierarchy.
- If tred package is instaled, the program will import the corresponing graph to .png files.

