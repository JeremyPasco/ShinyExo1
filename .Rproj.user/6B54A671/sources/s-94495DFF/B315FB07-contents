fluidPage(
  
  # Application title
  titlePanel("Old Faithful Geyser Data"),
  
  # Sidebar with a slider input for number of bins 
  sidebarLayout(
    sidebarPanel(
      
      dateRangeInput("date_filter",
                     "Date :",
                     min = "2013-01-01",
                     max = "2013-12-31",
                     start = "2013-01-01",
                     end = "2013-12-31"),
      
      sliderInput("arr_delay_filter",
                  "Retard : ",
                  value = c(-86, 1272),
                  min = -86,
                  max = 1272),
      
      numericInput("bins",
                   "Nombre de barres :",
                   value = 30,
                   min = 1,
                   max = 50)
    ),
    
    
    mainPanel(
      plotOutput("histo"),
      dataTableOutput("df")
    )
  )
)