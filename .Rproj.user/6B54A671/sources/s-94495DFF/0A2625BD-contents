library(tidyverse)
library(nycflights13)

function(input, output) {
  
  df <- reactive({
    
    print("A")
    
    flights %>%
      filter(
        time_hour >= input$date_filter[1],
        time_hour <= input$date_filter[2],
        arr_delay >= input$arr_delay_filter[1],
        arr_delay <= input$arr_delay_filter[2],
      )
  })
  
  output$histo <- renderPlot({
    
    print("B")
    
    df() %>% 
      ggplot() +
      geom_histogram(aes(x = air_time), bins = input$bins)
  })
  
  output$df <- renderDataTable({
    
    print("C")
    
    df()
  })
  
}