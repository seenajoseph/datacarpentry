#library("tidyverse")
str(surveys)
select(surveys,species_id,weight)
select(surveys,1,2)
filter(surveys,year==1995)
#%>s : 
  
  surveys %>% 
    filter(year==1995) %>% 
    select(species_id,weight) 
  
 (exercise <- surveys %>% 
    filter(weight < 5) %>% 
    select(species_id,sex,weight))
  
  surveys %>% 
   head(n = 5) %>% 
    select(species_id,sex,weight) 
  # create new column
  
  #mutate()
  
 data_with_kg <- surveys %>% 
    mutate(weight_kg=weight/1000)
 
surveys %>% 
   mutate(weight_kg=weight/1000, weight_kg2=weight_kg * 2) 
  

surveys %>% 
  mutate(weight_kg=weight/1000, weight_kg2=weight_kg * 2)  %>% 
  head(n=10)

new_d <- surveys %>% 
 filter(!is.na(weight)) %>%  mutate(weight_kg=weight/1000, weight_kg2=weight_kg * 2)
nrow(new_d)

surveys %>% 
  group_by(sex) %>% 
  summarise(mean_weight = mean(weight, na.rm=TRUE))

surveys %>% 
  filter(!(sex=="")) %>% 
  group_by(sex) %>% 
  summarise(mean_weight = mean(weight, na.rm=TRUE))

summarise_two <- surveys %>% 
  filter(!sex=="") %>% 
  filter(!is.na(weight)) %>% 
  group_by(sex,species_id) %>% 
  summarise(mean_weight=mean(weight))

summarise_four <- surveys %>% 
  filter(!sex=="") %>% 
  filter(!is.na(weight)) %>% 
  group_by(sex,species_id) %>% 
  summarise(mean_weight=mean(weight), min_weight=min(weight), mx_weight = max(weight))


summarise_five <- surveys %>% 
  filter(!sex=="") %>% 
  filter(!is.na(weight)) %>% 
  group_by(sex,species_id) %>% 
  summarise(mean_weight=mean(weight), min_weight=min(weight), mx_weight = max(weight), std_weight=sd(weight))

#counting

surveys %>% 
  filter (!sex=="") %>% 
  count(sex)

surveys %>% 
  filter (!sex=="") %>% 
  count(sex, species)

# sorting (arrange())
#reshaping the data


surveys %>% 
  filter (!sex=="") %>% 
  count(sex, species) %>% 
  arrange(species,desc(n))

surveys %>% 
  filter (!sex=="") %>% 
  count(sex, species) %>% 
  arrange(species,n)

plot(surveys$sex)

surveys_200<-surveys %>% 
   filter(!sex=="")  %>% 
   head(n=200)





