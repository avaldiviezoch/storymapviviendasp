<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Chart.js Línea – Prueba</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js@4.5.0/dist/chart.umd.min.js"></script>
  <style>
    html, body { height: 100%; margin: 0; background:#fff; }
    .wrap {
      min-height: 100%;
      display:flex; align-items:center; justify-content:center;
      padding:16px;
    }
    canvas { width:100%; max-width:900px; max-height:80vh; }
  </style>
</head>
<body>
  <div class="wrap">
    <canvas id="myChart"></canvas>
  </div>

  <script>
    // Meses en español
    const labels = ['Ene', 'Feb', 'Mar', 'Abr', 'May', 'Jun', 'Jul', 'Ago'];

    const data = {
      labels,
      datasets: [
        {
          label: 'Urbano',
          data: [12, 22, 35, 48, 65, 58, 73, 80],
          tension: 0.3,
          borderWidth: 3,
          pointRadius: 3,
          fill: false
        },
        {
          label: 'Rural',
          data: [8, 18, 20, 41, 55, 60, 62, 70],
          tension: 0.3,
          borderWidth: 3,
          pointRadius: 3,
          fill: false
        }
      ]
    };

    const config = {
      type: 'line',
      data,
      options: {
        responsive: true,
        interaction: {
          mode: 'index',
          intersect: false
        },
        plugins: {
          tooltip: {
            mode: 'index',
            intersect: false
          },
          title: {
            display: true,
            text: 'Comparativa Urbano vs Rural'
          },
          legend: { position: 'top' }
        },
        hover: {
          mode: 'index',
          intersect: false
        },
        scales: {
          x: {
            title: {
              display: true,
              text: 'Mes'
            }
          },
          y: {
            title: {
              display: true,
              text: 'Valor'
            },
            min: 0,
            max: 100,
            ticks: {
              stepSize: 50
            }
          }
        }
      }
    };

    window.addEventListener('DOMContentLoaded', () => {
      const ctx = document.getElementById('myChart');
      new Chart(ctx, config);
    });
  </script>
</body>
</html>
