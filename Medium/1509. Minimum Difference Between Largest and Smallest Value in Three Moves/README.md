#RU
<h1>Задача: Минимальная разница между наибольшим и наименьшим значением за три хода</h1>

<p>Эта задача решает задачу на LeetCode под номером 1509. Задача заключается в том, чтобы найти минимальную разницу между наибольшим и наименьшим значением массива <code>nums</code> после выполнения не более трех операций изменения элементов.</p>

<p>Ссылка на задачу на LeetCode: <a href="https://leetcode.com/problems/minimum-difference-between-largest-and-smallest-value-in-three-moves/" target="_blank">1509. Minimum Difference Between Largest and Smallest Value in Three Moves</a></p>

<h2>Решение</h2>

<h3>Описание</h3>

<p>Для решения задачи мы используем следующий подход:</p>

<ol>
    <li><strong>Сортировка массива:</strong> Начнем с сортировки массива <code>nums</code>. Это позволит нам легко найти наименьшие и наибольшие элементы.</li>
    <li><strong>Нахождение минимальной разницы:</strong> После сортировки рассматриваем возможные комбинации изменений в трех наименьших и трех наибольших элементах массива. Целью является минимизация разницы между наибольшим и наименьшим значениями после изменений.</li>
    <li><strong>Реализация алгоритма:</strong> В решении используется класс <code>Solution</code> с методом <code>minDifference</code>, который принимает массив <code>nums</code> и возвращает минимальную разницу. Мы вычисляем разницу для четырех возможных комбинаций:
        <ul>
            <li>Замена трех наибольших элементов на три наименьших.</li>
            <li>Замена двух наибольших и одного среднего элемента на три наименьших.</li>
            <li>Замена одного наибольшего и двух средних элементов на три наименьших.</li>
            <li>Замена трех наименьших элементов на три наибольших.</li>
        </ul>
    </li>
</ol>

<h3>Примеры использования</h3>

<pre><code>solver = Solution();

nums1 = [5, 3, 2, 4]
nums2 = [1, 5, 0, 10, 14]
nums3 = [3, 100, 20]

print(solver.minDifference(nums1))  # Ожидаемый вывод: 0
print(solver.minDifference(nums2))  # Ожидаемый вывод: 1
print(solver.minDifference(nums3))  # Ожидаемый вывод: 0
</code></pre>
<h2>Сложность</h2>

<p><strong>Временная сложность:</strong> O(n log n)</p>

<p>Решение включает сортировку массива, которая имеет временную сложность O(n log n) из-за операции сортировки. После сортировки алгоритм выполняет операции за постоянное время для вычисления минимальной разницы, что общая временная сложность составляет O(n log n), где n - количество элементов в массиве <code>nums</code>.</p>

<p><strong>Пространственная сложность:</strong> O(1)</p>

<p>Алгоритм использует только постоянное количество дополнительной памяти, преимущественно для переменных и временного хранения во время вычислений. Это приводит к общей пространственной сложности O(1), что означает, что использование памяти остаётся постоянным независимо от размера входных данных.</p>

#EN
<h1>Problem: Minimum Difference Between Largest and Smallest Value in Three Moves</h1>

<p>This problem addresses LeetCode problem number 1509. The task is to find the minimum difference between the largest and smallest values in the array <code>nums</code> after performing at most three operations to change elements.</p>

<p>Link to the problem on LeetCode: <a href="https://leetcode.com/problems/minimum-difference-between-largest-and-smallest-value-in-three-moves/" target="_blank">1509. Minimum Difference Between Largest and Smallest Value in Three Moves</a></p>

<h2>Solution</h2>

<h3>Description</h3>

<p>To solve the problem, we use the following approach:</p>

<ol>
    <li><strong>Sorting the array:</strong> Start by sorting the array <code>nums</code>. This allows us to easily identify the smallest and largest elements.</li>
    <li><strong>Finding the minimum difference:</strong> After sorting, consider possible combinations of changes to the three smallest and three largest elements of the array. The goal is to minimize the difference between the largest and smallest values after changes.</li>
    <li><strong>Algorithm implementation:</strong> The solution uses a class <code>Solution</code> with a method <code>minDifference</code>, which takes the array <code>nums</code> and returns the minimum difference. We calculate the difference for four possible combinations:
        <ul>
            <li>Replacing the three largest elements with the three smallest.</li>
            <li>Replacing two largest and one middle element with the three smallest.</li>
            <li>Replacing one largest and two middle elements with the three smallest.</li>
            <li>Replacing the three smallest elements with the three largest.</li>
        </ul>
    </li>
</ol>

<h3>Usage Examples</h3>

<pre><code>let solver = new Solution();

let nums1 = [5, 3, 2, 4];
let nums2 = [1, 5, 0, 10, 14];
let nums3 = [3, 100, 20];

console.log(solver.minDifference(nums1));  // Expected output: 0
console.log(solver.minDifference(nums2));  // Expected output: 1
console.log(solver.minDifference(nums3));  // Expected output: 0
</code></pre>

<h2>Complexity</h2>

<p><strong>Time complexity:</strong> O(n log n)</p>

<p>The solution involves sorting the array, which has a time complexity of O(n log n) due to the sorting operation. After sorting, the algorithm performs constant time operations to calculate the minimum difference, resulting in an overall time complexity of O(n log n), where n is the number of elements in the array <code>nums</code>.</p>

<p><strong>Space complexity:</strong> O(1)</p>

<p>The algorithm uses only a constant amount of extra space, primarily for variables and temporary storage during calculations. This results in an overall space complexity of O(1), meaning the space usage remains constant regardless of the input size.</p>