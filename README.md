# Cost-analysis-production-management
Optimization of a linear programming model with Highs solver
A small metal parts shop contains three machines a drill press, a lathe and grinder - and has three operators, each certified to work on all three machines. However, each operator performs better on some machines than on others. The shop has contracted to do a big job that requires all three machines. The times required by the various operators to perform the required operations on each machine are summarized as follows:
Operator 1, Drill Press(min): 22, Lathe(min): 18, Grinder(min): 35
Operator 2, Drill Press(min): 29, Lathe(min): 30, Grinder(min): 28
Operator 3, Drill Press(min): 25, Lathe(min): 36, Grinder(min): 18
Requirements: The shop keeper wants to minimize the total operating time which is the sum of the time spent by each operator on their respective machines. The linear programming can be formulated as follows:
# Coefficients of the objective function (total operating time)
c = [22, 18, 35, 29, 30, 28, 25, 36, 18]
Solution using the linear programming code used below: 
Used scipy and Python for the linprog function from the scipy.optimize module to solve the linear programming problem. The optimal solution, including the total operating time and the operator-machine assignment matrix, will be printed.

I have used ‘Highs solver’ to optimize this problem in Linear programming. As we know highs is one of the efficient Algorithm used to optimize the problems by bringing out the highest or the lowest outcomes. It is simply used to increase the efficiency of various factors.

Optimal Solution:
Total Operating Time: 65.0
Operator-Machine Assignment Matrix:
Operator 1 on Machine 1: 0.0
Operator 1 on Machine 2: 1.0
Operator 1 on Machine 3: 0.0
Operator 2 on Machine 1: 1.0
Operator 2 on Machine 2: -0.0
Operator 2 on Machine 3: -0.0
Operator 3 on Machine 1: 0.0
Operator 3 on Machine 2: 0.0
Operator 3 on Machine 3: 1.0




Summary:
Total Operating Time: The optimal solution results in a total operating time of 65.0 units.

Operator-Machine Assignment Matrix: The assignment matrix indicates the optimal assignment of operators to machines. Each row corresponds to an operator, and each column corresponds to a machine. The values represent the time spent by each operator on each machine.

Operator 1 is assigned to Machine 2.
Operator 2 is assigned to Machine 1.
Operator 3 is assigned to Machine 3.
The values are expected to be 0 or 1, indicating the assignment or non-assignment of an operator to a machine. However, due to potential numerical precision issues in the optimization solver, values like -0.0 may appear, and these can be treated as 0.

Conclusion:
The linear programming model has been successfully solved, and the optimal solution indicates the most efficient assignment of operators to machines, minimizing the total operating time. In this case, Operator 1 is assigned to Machine 2, Operator 2 to Machine 1, and Operator 3 to Machine 3, resulting in a total operating time of 65.0 units.
The negative zero values in the output are likely artifacts of the numerical optimization process and can be interpreted as zero. Overall, the solution meets the constraints of the problem and provides an optimized assignment strategy for the given scenario.

