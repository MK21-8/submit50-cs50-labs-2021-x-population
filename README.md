# submit50-cs50-labs-2021-x-population
Population
#include <cs50.h>
#include <stdio.h>

//  Obtain number of years taken from start population to end

int start_population(void);
// end population must be more than start
int main(void)
{
    int n = start_population();
    int x;
    do
    {
        x = get_int("end size: \n");
    }
    while (x < n);

// calculate number of years

    int i = 0;
    for (i = 0; n < x; i++)
    {
        n = n + (n / 3) - (n / 4);
    }

    printf("Years: %i\n", i);

}
// Start size to be above 8
int start_population(void)
{
    int n;
    do
    {
        n = get_int("start size: \n");
    }
    while (n < 9);
    return n;
}
