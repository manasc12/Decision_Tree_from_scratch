# Decision_Tree_from_scratch
- Building Decision Tree algorithm without using any machine learning library to predict survival of Titanic passengers.
  - Here I have used **Entropy Value** of each attribute to create our decision tree.
  - The dataset used here is from **Kaggle**: [Titanic Passenger Datset Link](https://www.kaggle.com/c/titanic)
## Methods that I have used to create decision tree
### Top-Down Induction of Decision Trees:
- Learn Trees in a Top-Down Fashion
  - Divide the problem in sub problems
  - solve each problem
  ![Divide-and-Conquer Approach](Divide-And-Conquer.png)
### What is a Good Attribute for a Node?
- We want to grow a simple Tree.
  - a good attribute prefers attributes that splits the data so that each successor node is as pure as possible
- In other words:
  - We want a measure that prefers attributes that have high degree of order
    - Maximum Order: All examples are of the same Class
    - Minimum Order: All Classes are equally likely
  - **Entropy** is a measure of (un-)orderedness
  - Another interpretation:
    - Entropy is the amount of information that is contained
    - All examples of the same class -> no information
    - s is a set of examples
    - p<sub>(+)</sub> is the propertion of examples in class '+'
    - p<sub>(-)</sub> is the propertion of examples in class '-'
    - p<sub>(-)</sub>=1-p<sub>(+)</sub> 
    - **Entropy** E(s) = -p<sub>(+)</sub>log<sub>2</sub> p<sub>(+)</sub> - p<sub>(-)</sub>log<sub>2</sub> p<sub>(-)</sub> 
    - Interpretation :
      - Amount of unorderedness in the class distribution of s
      ![Entropy_Calculation_plus_minus.png](Entropy_Calculation_plus_minus.png)
      - Entropy can be easily generated for classes n>2 
        - p<sub>(i)</sub> is the proportion of the examples in s that belongs to i-th class
        - E(s) = -p<sub>(1)</sub>log<sub>2</sub> p<sub>(1)</sub> - p<sub>(2)</sub>log<sub>2</sub> p<sub>(2)</sub> ... - p<sub>(n)</sub>log<sub>2</sub> p<sub>(n)</sub> = 	\sum
##  References
- Analytical Information Systems course by **Prof. Dr. Gefei Zhang** at **Hochschule Hof**
    - [Link to Profile: **Prof. Dr. Gefei Zhang**](https://people.f4.htw-berlin.de/~zhangg/)
    - [Link to Course Description at **Hochschule Hof, Bavaria**](https://www.hof-university.com/graduate-school/masters-program-full-time/software-engineering-for-industrial-applications-meng.html)
