You are given an integer array height of length n. There are n vertical lines drawn such that the two endpoints of the ith line are (i, 0) and (i, height[i]).

Find two lines that together with the x-axis form a container, such that the container contains the most water.

Return the maximum amount of water a container can store.

Notice that you may not slant the container.

Implement with two pointer:
c_Area(height[], a, b){
  return min(height[a], height[b]) *(|b-a|)
}

Initial Area = 0, High = 0, Low = 0 max_index = sizeof(array) min_index = 0
Initial High = height[max_index]; Low = height[min_index]
Initial Area = max_index - low_index
min_index++
if(height[min_index] > height[min_index--]){
  inter = c_Area(height, min_index, max_index)
  if (inter > Area){
    Area = inter
  }
}
else{
  
}
