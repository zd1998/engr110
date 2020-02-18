<html>
  <head>
    <script src="https://cdn.jsdelivr.net/npm/chart.js@2.8.0"></script>
  </head>
  <body>
    <div width='200' height='200'>
      <canvas id="myChart"></canvas>
      <script>
        var ctx = document.getElementById('myChart').getContext('2d');
        var chart = new Chart(ctx, {
    // The type of chart we want to create
          type: 'line',
    // The data for our dataset
          data: {
            labels: ['72Hrs ago', '60Hrs ago', '48Hrs ago', '36Hrs ago', '24Hrs ago', '12Hrs ago', 'Now'],
            datasets: [{
              fill: false,
              lineTension: 0,
              label: 'Beehive 1',
              backgroundColor: 'rgb(255, 99, 132)',
              borderColor: 'rgb(255, 99, 132)',
              data: [240,245,242,240,200,190,190],
              pointRadius: 20,
              pointHoverRadius: 20
            },
            {
              fill: false,
              lineTension: 0,
              label: 'Beehive 2',
              backgroundColor: 'rgb(132, 99, 255)',
              borderColor: 'rgb(132, 99, 255)',
              data: [270,265,268,265,263,265,254],
              pointRadius: 20,
              pointHoverRadius: 20
            }]
          },
    // Configuration options go here
          options: {
            responsive: true,
            title: {
              display: true,
              text: 'Forge Garden Hive Weight'
            },
            scales: {
              xAxes: [{
                display: true,
                scaleLabel: {
                  display: true,
                  labelString: 'Time'
                }
              }],
              yAxes: [{
                display: true,
                scaleLabel: {
                  display: true,
                  labelString: 'Weight(Pounds)'
                },
                ticks: {
                    beginAtZero: true
                }
              }]
            }
          }
        });
      </script>
    </div>
  </body>
</html>
