https://anydice.com/program/1f584

\output [lowest 2 of 3d10] named "2d10, disadvantage"
output 2d10 named "2d10"
output [highest 2 of 3d10] named "2d10, advantage"


loop X over {4,6,8}{
 output [lowest 2 of 3d10]-dX named "2d10-d[X], disadvantage"
 output 2d10-dX named "2d10-d[X]"
 output [highest 2 of 3d10]-dX named "2d10-d[X], advantage"

 output [lowest 2 of 3d10]+dX named "2d10+d[X], disadvantage"
 output 2d10+dX named "2d10+d[X]"
 output [highest 2 of 3d10]+dX named "2d10+d[X], advantage"
}\
\
loop N over {3..6}{
K: N-2
output [lowest 2 of Nd10] named "2d10, disadvantage [K]"
output [highest 2 of Nd10] named "2d10, advantage [K]"
}
output 2d10 named "2d10"\

\ABILITIES: 6 d (3d6)
loop P over {1..6} {
 output P @ ABILITIES named "3d6 [P]"
}\

\ABILITIES: 6 d [highest 3 of 4d6]
loop P over {1..6} {
 output P @ ABILITIES named "4d6k3 [P]"
}\

X: 5 d (10d10)
loop P over {1..6} {
 output P @ X named "10d10 [P]"
}

////////////////////////////////////////////////////////////////////////////////

\output [lowest 2 of 3d10] named "2d10, disadvantage"
output 2d10 named "2d10"
output [highest 2 of 3d10] named "2d10, advantage"


loop X over {4,6,8}{
 output [lowest 2 of 3d10]-dX named "2d10-d[X], disadvantage"
 output 2d10-dX named "2d10-d[X]"
 output [highest 2 of 3d10]-dX named "2d10-d[X], advantage"

 output [lowest 2 of 3d10]+dX named "2d10+d[X], disadvantage"
 output 2d10+dX named "2d10+d[X]"
 output [highest 2 of 3d10]+dX named "2d10+d[X], advantage"
}\
\
loop N over {3..6}{
K: N-2
output [lowest 2 of Nd10] named "2d10, disadvantage [K]"
output [highest 2 of Nd10] named "2d10, advantage [K]"
}
output 2d10 named "2d10"\

\ABILITIES: 6 d (3d6)
loop P over {1..6} {
 output P @ ABILITIES named "3d6 [P]"
}\

\ABILITIES: 6 d [highest 3 of 4d6]
loop P over {1..6} {
 output P @ ABILITIES named "4d6k3 [P]"
}\

\X: 5 d (10d10)
loop P over {1..6} {
 output P @ X named "10d10 [P]"
}\
\
loop DC over {12..20}{
output 2d10+5 >= DC named "2d10 hits [DC]"
}


loop DC over {12..20}{
output d20+5 >= DC named "d20 hits [DC]"
}
\

