### Hi, My name is Venkatanarayanan 👋
#
I am a Data Analyst with specific interest in Data Visualisation. My Data Analysis journey started roughly three years back and since then I have created numerous visualisations using R and other tools. I have created these visuals not just for me but also for others as a part of my freelance work. I have thoroughly enjoyed this journey and I am always looking to learn more. I am available to consult for Data Analytics / Data Visualisation

### Tools I use everyday ###
#
* R Programming
* Shiny

```{r}
data.frame(skill = c("Data Visualization", "Data Wrangling",
                     "R Programming", "Shiny",
                     "Python for Data Science", "Tableau"),
           percent = c(90, 80, 80, 50, 25, 25)) %>%
  mutate(non_percent = 100 - percent) %>%
  gather(key, value, -skill) %>%
  ggplot(aes(x = 2, y = value, fill = key)) +
  geom_bar(stat = "identity",
           color = "gray27") +
  geom_text(aes(label = ifelse(key == "percent", paste0(value, "%"), ""),
                x = 0.5,
                y = 0),
            size = 3.5,
            family = "Tahoma",
            color = "ivory1",
            fontface = "bold") +
  facet_wrap(~factor(skill,
                     levels = c("Data Visualization", "Data Wrangling",
                                "R Programming", "Shiny",
                                "Python for Data Science", "Tableau")),
             ncol = 6) +
  coord_polar("y", start = 0) +
  xlim(.2,2.5) +
  scale_fill_manual(values = c("percent" = "goldenrod1",
                               "non_percent" = "#0e0f0b")) +
  theme(
    legend.position = "none",
    legend.title = element_blank(),
    legend.text = element_text(family = "Tahoma",
                               size = 12,
                               color = "ivory1",
                               face = "bold"),
    legend.background = element_rect(fill = "#0e0f0b",
                                     color = "#0e0f0b"),
    legend.key = element_rect(fill = "#0e0f0b",
                              size = 8),
    legend.margin = margin(0,0,0,0),
    plot.background = element_rect(fill = "#0e0f0b",
                                   color = "#0e0f0b"),
    plot.margin =  margin(20, 20, 20, 20, "pt"),
    panel.background = element_rect(fill = "#0e0f0b"),
    axis.ticks = element_blank(),
    panel.grid.major.x = element_blank(),
    panel.grid.major.y = element_blank(),
    panel.grid.minor = element_blank(),
    axis.text.x = element_blank(),
    axis.text.y = element_blank(),
    axis.title = element_blank(),
    strip.background = element_rect(fill = "#0e0f0b"),
    strip.text = element_text(color = "ivory1",
                              size = 10,
                              family = "Tahoma",
                              face = "bold"),
    plot.title = element_text(color = "ivory1", 
                              size = 12, 
                              margin = margin(0, 0, 10, 0, "pt"), 
                              hjust = 0.5,
                              family = "Tahoma",
                              face = "bold"),
    plot.subtitle = element_text(color = "ivory1", 
                                 size = 14, 
                                 margin = margin(0, 0, 20, 0, "pt"), 
                                 hjust = 0.5,
                                 family = "Tahoma",
                                 face = "bold")
  )
  
```  

### Projects I have worked on so far ###
#
:white_check_mark: A Shiny [Application](http://165.22.210.69:3838/age-profile-app/) which serves as a scouting tool for EPL Players using data from fbref. Please note that this tool is still under development.


### :speaker: How to reach out to me? ###
#
* [Twitter](https://twitter.com/VenkyReddevil)
* [Linkedin](https://www.linkedin.com/in/venkatanarayanan-v-533643ba/)
* [Blog](https://footytistics.com/)
