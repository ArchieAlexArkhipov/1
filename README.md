#include <stdio.h> 
#include <math.h>
const double POISON = tan(M_PI/2);
const double EPS    = DBL_ERSILON;
const int INFINITE_ROOTS = -1;

int main()
{
  printf("Solve quadratic equation @archie\n"
         "Enter coefficients a, b, c as numbers:");
  double a = POISON, b = POISON, c = POISON;
  scanf("%lg %lg %lg", &a, &b, &c);
  assert(a != POISON);
  assert(b != POISON);
  assert(c != POISON);
  
  double root1 = POISON, root2 = POISON;
  int TheNumberOfRoots = NumberOfRoots(a, b, c, &root1, &root1);
  
}
int NumberOfRoots(double a, double b, double c, double* x1, double* x2)
{
  assert(x1);
  assert(x2);
  assert(x1 != x2);
  
  if ((a == 0) && (b == 0) && (c == 0))
    NumberOfRoots = INFINITE_ROOTS;
  else
    if (a == 0)
      NumberOfRoots = 1;
  if (b*b - 4*a*c > 0)
    NumberOfRoots = 2;
  if (b*b - 4*a*c == 0)
    NumberOfRoots = 1;
  if (b*b - 4*a*c < 0)
    NumberOfRoots = 0;
}

