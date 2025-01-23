<h2>Quick Sorting</h2>

<h3>1. Choose a Pivot</h3>
<p>Select an element from the array as the pivot. Common choices are:</p>
<ul>
    <li>The first element.</li>
    <li>The last element.</li>
    <li>A random element.</li>
    <li>The median element.</li>
</ul>

<h3>2. Partition the Array</h3>
<p>Rearrange the elements so that:</p>
<ul>
    <li>All elements less than or equal to the pivot are placed on the left side.</li>
    <li>All elements greater than the pivot are placed on the right side.</li>
</ul>
<p>Place the pivot in its correct position in the sorted array.</p>

<h3>3. Recursively Sort Subarrays</h3>
<p>Recursively apply the same process to the subarray on the left of the pivot and the subarray on the right of the pivot.</p>

<h3>4. Base Case</h3>
<p>The recursion terminates when the subarray has one or zero elements (i.e., it is already sorted).</p>

<hr>

<h3>Detailed Steps</h3>

<h4>1. Partitioning</h4>
<p>Let the chosen pivot be <code>arr[pivotIndex]</code>.</p>
<p>Initialize two pointers, <code>i</code> and <code>j</code>:</p>
<ul>
    <li><code>i</code> starts at the beginning of the array (or the subarray).</li>
    <li><code>j</code> scans the array for elements less than or equal to the pivot.</li>
</ul>
<p>If <code>arr[j]</code> is less than or equal to the pivot, increment <code>i</code> and swap <code>arr[i]</code> and <code>arr[j]</code>.</p>
<p>After the loop, swap <code>arr[i + 1]</code> with the pivot element, placing the pivot in its correct position.</p>

<h4>2. Recursion</h4>
<p>Apply the quick sort recursively to the left subarray (<code>arr[low...pivotIndex-1]</code>) and the right subarray (<code>arr[pivotIndex+1...high]</code>).</p>

<h4>3. Repeat</h4>
<p>Repeat the partition and recursive steps until the entire array is sorted.</p>


