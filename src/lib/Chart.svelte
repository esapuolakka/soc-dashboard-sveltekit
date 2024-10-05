<script lang="ts">
  import { Line } from 'svelte-chartjs';
  import { Chart as ChartJS, LineElement, CategoryScale, LinearScale, PointElement, Tooltip, Legend } from 'chart.js';

  // Register the chart elements to use
  ChartJS.register(LineElement, CategoryScale, LinearScale, PointElement, Tooltip, Legend);

  // Define the chart data
  export let data = {
    labels: ['January', 'February', 'March', 'April', 'May'],
    datasets: [
      {
        label: 'My First Dataset',
        data: [65, 59, 80, 81, 56],
        fill: false,
        borderColor: 'rgb(75, 192, 192)',
        tension: 0.1
      }
    ]
  };

  // Define the chart options
  export let options = {
    responsive: true,
    maintainAspectRatio: false
  };
</script>

<!-- Chart rendering container -->
<div style="position: relative; height: 40vh; width: 80vw">
  <Line {data} {options} />
</div>
