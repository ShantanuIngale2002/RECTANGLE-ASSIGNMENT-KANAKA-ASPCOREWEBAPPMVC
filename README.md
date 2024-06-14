This assignment is given by Niranjan Aradhye sir in Kanaka on 14 June 2024.

THe goal is to solve a coding problem name "maximum value" using technology.

IMPLEMENTATION IN TECHNOLOGY >>>>>
1. Created a repo pattern and initialized whole project.
2. Created a view to get row, column and test case input and another view to show all records.
3. Successful calculation of getting a answer results in saving the current record in database as well.

CODE PROBLEM >>>>>
Given is a matrix denoting a weighted table.
Find a rectangle of sides of length at least 2, such that the minimum weight from the 4 corners of the rectangle is maximized.
That is for the table A[N][M], find the maximum value of MIN(A[i1][j1], A[i1][j2], A[i2][j1], A[i2][j2]) such that 1 <= i1 < i2 <= N and 1 <= j1 < j2 <= M.
Find the minimum weight from the 4 corners of the rectangle that is maximized.

Sample test case explaination >>>>>
FOR THIS TEST CASE
M, N = 5,4
A = [[1,8,3,5],[2,5,4,2],[3,4,5,6],[1,4,2,6],[2,8,1,7]]

Since atleast 2 sides but from fundamental if we check all values the explicitly whole matrix gets covered anyway.
Hence we will perform fudamental min of 4 elements as
max=0
at any i,j do
	min = MIN(min(A[i][j], A[i+1][j], A[j][i+1], A[i+1][j+1])
	if min > max : max = min
return max

like for i=0,j=0
consider 
A[0][0] = 1
A[0][1] = 8
A[1][0] = 2
A[1][1] = 5
minimum is 1 ie. > max:0 hence max=1
likewise if we do this for all i,j
finally in rectangle
8 3 5
5 4 2
4 5 6
4 2 6
8 1 7
min(Corners) = 5 ie > max:any hence max=5 (which is sol)


Python practice implementation >>>>>>
M, N = 5,4
A = [[1,8,3,5],[2,5,4,2],[3,4,5,6],[1,4,2,6],[2,8,1,7]]
maxValue = 0
for i in range(M-2):
    for j in range(N-2):
        currMin = min(A[i][j], A[i+1][j], A[j][i+1], A[i+1][j+1])
        if currMin > maxValue:
            maxValue = currMin
print(maxValue)






