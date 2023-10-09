 void shift();
 void display();
 #define Right  1
 # define Left  0
// int main()
{
    int n= 5;
 int a[n],b[n],i,c,j;
 printf("Enter The Numbers:");
 for(i=0;i<n;i++){
 scanf("%d",&a[i]);
 }
 for(i=0;i<n;i++)
 {
     c=1;
     if(a[i] != -1)
     {
         for(j=i+1;j<n;j++)
     {
         if(a[i] == a[j])
         {
             c++;
             a[j]= -1;
         }
     }
     b[i] = c;
     }
 }
 for(i=0;i<n;i++)
 {
     if(a[i] != -1)
     {
         printf("No of %d is %d",a[i],b[i]);
     }
 }
    return 0;
}

int main()

{
    printf("enter the  number:");
    int n=5;
    int a[n],i,j,k;
    for(i=0;i<n;i++){
    scanf("%d",&a[i]);
    }
    for(i=0;i<n;i++)
    {
        for(j=i+1;j<n;j++)
        {
            if(a[i] == a[j])
            {
                for(k=j;k<n;k++)
                {
                    a[k] = a[k+1];
                }
                n--;
                k--;
            }
        }
    }
    for(i=0;i<n;i++){
    printf("%d",a[i]);
    }
}

void shift(int a[],int n,int dir,int counter)
{
    int temp,i;
    if(dir == Right){
        temp = a[n-1];
        while(counter)
        {
            for(i=n-1;i>=1;i--)
            a[i] = a[i-1];
            a[0] = temp;
            counter--;
        }
    }
    else
    {
        temp = a[0];
        while(counter)
        {
            for(i=0;i<n;i++)
            a[i] = a[i+1];
            a[n-1] = temp;
            counter--;
        }
    }
}

void display(int a[], int n)
{
    int i;
    for(i = 0;i<n;i++)
    {
        printf("%d",a[i]);
    }
}

int main()
{
    printf("enter the Number:");
    int n = 5;
    int a[n],i;
    for(i=0;i<n;i++){
        scanf("%d",&a[i]);
    }
    display(a,n);
    printf("\n");
    shift(a,n,Left,3);
    printf("\n");
    display(a,n);
    return 0;
}

int main()
{
    int n = 5;
    int a[n],i;
    printf ("Enter the nummber:");
    for(i=0;i<n;i++)
    {
        scanf("%d",&a[i]);
    }
    for(i=n-1;i>=0;i--)
    {
        printf("%d",a[i]);
    }
    return 0;
}

