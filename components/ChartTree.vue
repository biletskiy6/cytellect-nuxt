<template>
  <div id="chartdiv" ref="chartdiv" class="project-chart"></div>
</template>

<script>
import * as am4core from '@amcharts/amcharts4/core'
// eslint-disable-next-line no-unused-vars
import * as am4charts from '@amcharts/amcharts4/charts'
// eslint-disable-next-line camelcase
import am4themes_animated from '@amcharts/amcharts4/themes/animated'
// eslint-disable-next-line camelcase
import * as am4plugins_forceDirected from '@amcharts/amcharts4/plugins/forceDirected'

am4core.useTheme(am4themes_animated)
export default {
  name: 'ChartTree',
  mounted() {
    const chart = am4core.create(
      'chartdiv',
      am4plugins_forceDirected.ForceDirectedTree
    )
    // chart.legend = new am4charts.Legend()
    // chart.legend.markers.template.disabled = true
    // chart.legend.labels.template.propertyFields.fill = 'red'
    // chart.legend.labels.template.propertyFields.stroke = 'red'

    const networkSeries = chart.series.push(
      new am4plugins_forceDirected.ForceDirectedSeries()
    )

    networkSeries.data = [
      {
        name: 'Project Alpha',
        fixed: true,
        disabled: false,
        x: am4core.percent(50),
        y: am4core.percent(50),
        children: [
          {
            name: '#1',
            value: 1,
            children: [
              {
                name: 'Task 1',
                type: 'image',
                image:
                  'https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSpjK_9TLSIcg9qPaw5ZDrJT3c8lXTxtp8ESg&usqp=CAU'
              },
              { name: 'Task 2' },
              { name: 'Task 3' },
              {
                name: 'Task 4',
                children: [
                  {
                    name: 'Subtask 1'
                  },
                  {
                    name: 'Subtask 2'
                  }
                ]
              }
            ]
          },
          {
            name: '#2',
            value: 1,
            children: [
              { name: 'Task 1' },
              {
                name: 'Task 2',
                children: [
                  {
                    name: 'Subtask 1'
                  },
                  {
                    name: 'Subtask 2'
                  }
                ]
              }
            ]
          },
          {
            name: '#3',
            value: 1,
            children: [
              { name: 'Task 1' },
              {
                name: 'Task 2',
                children: [
                  {
                    name: 'Subtask 1'
                  },
                  {
                    name: 'Subtask 2'
                  }
                ]
              }
            ]
          },
          {
            name: 'Problem',
            value: 1,
            children: [
              { name: 'Problem 1' },
              {
                name: 'Problem 2'
              }
            ]
          }
        ]
      }
    ]

    networkSeries.dataFields.linkWith = 'linkWith'
    networkSeries.dataFields.name = 'name'
    networkSeries.dataFields.id = 'name'
    networkSeries.dataFields.value = 'value'
    networkSeries.dataFields.children = 'children'

    networkSeries.nodes.template.tooltipText = '{name}'
    networkSeries.nodes.template.fillOpacity = 1
    networkSeries.nodes.template.label.text = '{name}'
    networkSeries.fontSize = 10
    networkSeries.minRadius = 20

    networkSeries.maxLevels = 2
    networkSeries.legendSettings.labelText = '[{stroke}]{name}[/]'

    // networkSeries.maxRadius = am4core.percent(1)
    // networkSeries.centerStrength =
    // networkSeries.nodes.template.label.hideOversized = true
    networkSeries.nodes.template.label.truncate = true

    // networkSeries.events.on('inited', function() {
    //   networkSeries.animate(
    //     {
    //       property: 'velocityDecay',
    //       to: 1
    //     },
    //     3000
    //   )
    // })

    // Configure icons
    const icon = networkSeries.nodes.template.createChild(am4core.Image)
    icon.propertyFields.href = 'image'
    icon.horizontalCenter = 'middle'
    icon.verticalCenter = 'middle'
    icon.width = 60
    icon.height = 60

    // const nuxt = this.$nuxt
    networkSeries.nodes.template.events.on('hit', function(event) {
      // eslint-disable-next-line no-console
      console.log(event.target.dataItem)
      // chart.zoomToDataItem(event.target.dataItem, 1.1, true)
    })
  }
}
</script>
