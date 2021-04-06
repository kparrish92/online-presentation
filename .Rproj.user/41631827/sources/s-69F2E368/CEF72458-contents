library(tibble)
library(dplyr)

g_o_t1 = tibble(accuracy = rnorm(166,.4,.49)) %>% 
  mutate(time = "t1", feature = "obstruent", language = "german") 


g_r_t1 = tibble(accuracy = rnorm(97,.73,.41)) %>% 
  mutate(time = "t1", feature = "rhotic", language = "german")


g_o_t2 = tibble(accuracy = rnorm(159,.44,.50)) %>% 
  mutate(time = "t2", feature = "obstruent", language = "german") 


g_r_t2 = tibble(accuracy = rnorm(94,.4,.46)) %>% 
  mutate(time = "t2", feature = "rhotic", language = "german")



e_o_t1 = tibble(accuracy = rnorm(162,.5,.52)) %>% 
  mutate(time = "t1", feature = "obstruent", language = "english") 


e_r_t1 = tibble(accuracy = rnorm(99,.91,.29)) %>% 
  mutate(time = "t1", feature = "rhotic", language = "english")


e_o_t2 = tibble(accuracy = rnorm(162,.5,.52)) %>% 
  mutate(time = "t2", feature = "obstruent", language = "english") 


e_r_t2 = tibble(accuracy = rnorm(99,.91,.29)) %>% 
  mutate(time = "t2", feature = "rhotic", language = "english")


fake_data = rbind(g_o_t1, g_o_t2, g_r_t1, g_r_t2, e_o_t1, e_o_t2, e_r_t1, e_r_t2)

library(ggplot2)

fake_data %>% 
  ggplot(aes(y = accuracy, x = language, color = feature, fill = time)) + geom_boxplot()

# show rhotics only

fake_data %>% 
  filter(feature == "rhotic") %>% 
  ggplot(aes(y = accuracy, x = language, color = time)) + geom_boxplot()


fake_data %>% 
  filter(feature == "rhotic") %>%
  ggplot(aes(y = accuracy, x = language, color = time)) +
  stat_summary(fun.data = "mean_cl_boot") + geom_point(alpha = .02, color = "black") + 
  ggtitle("Hypothetical graph of rhotic variation at T1 and T2") + 
  ylim(0,1)


# obstruent devoicing 

fake_data %>% 
  filter(feature == "obstruent") %>%
  ggplot(aes(y = accuracy, x = language, color = time)) +
  stat_summary(fun.data = "mean_cl_boot") + geom_point(alpha = .02, color = "black") + 
  ggtitle("Hypothetical graph of obstruent devoicing variation at T1 and T2") + 
  ylim(0,1)

fake_data %>% 
  filter(feature == "obstruent") %>%
  ggplot(aes(y = accuracy, x = language, color = time)) + geom_boxplot() + 
  ggtitle("Hypothetical graph of rhotic variation at T1 and T2") + 
  ylim(0,1)



fake_data %>% 
  filter(feature == "rhotic") %>%
  ggplot(aes(y = accuracy, x = language, color = time)) + geom_boxplot() + 
  ggtitle("Hypothetical graph of rhotic variation at T1 and T2") + 
  ylim(0,1)

