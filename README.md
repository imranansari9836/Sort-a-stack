# Sort-a-stack
Given a stack, the task is to sort it such that the top of the stack has the greatest element.

Example 1:

Input:
Stack: 3 2 1
Output: 3 2 1
Example 2:

Input:
Stack: 11 2 32 3 41
Output: 41 32 11 3 2

class GfG{
	public Stack<Integer> sort(Stack<Integer> s)
	{
		//add code here.
	 int n = s.size();
   int arr[]=new int[n];
   int k = 0;
   while(!s.empty()){
       arr[k++] = s.peek();
       s.pop();
   }
   for(int i = 0; i < n; i++){
       for(int j = i; j < n; j++){
           if(arr[i] > arr[j]){
               int temp = arr[i];
               arr[i] = arr[j];
               arr[j] = temp;
           }
       }
   }
   for(int i = 0; i < n; i++){
       s.push(arr[i]);
   }
   return s;
}
}
