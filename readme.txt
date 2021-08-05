const lineChart = (
    dailyData.length
    ? (
      <Line
       data={{
         labels: dailyData(({ date }) => date),
         datasets: [{
           data: dailyData(( { confirmed }) => confirmed),
           label: 'Infected',
           borderColor: '#3333ff',
           fill: true,
         }, {
          data: dailyData(( { deaths }) => deaths),
          label: 'Infected',
          borderColor: 'red',
          backgroundColor: 'rgba(255, 0, 0, 0.5)',
          fill: true,
         }],
       }}
    /> ) : null
  );

const lineChart = dailyData[0] ? (
    <Line
      data={{
        labels: dailyData(({ date }) => date),
        datasets: [{}, {}],
      }}
    />
  ) : null;
