# Data Science Cheet Sheet

----
## Pandas

---

**Summarizing numerical data:**
.agg([*functions in here*])--use multiple functions
.median(),.mode()  
.min(),.max()  
.var(),.std()  
.sum()  
.quantile()  

---



dogs.head() --- 5 top lines

dogs.shape --- width and height of the chart

dogs.sort_values("weight_kg"", ascending=(True/false))
dogs.sort_values(["weight_kg", "height_cm"], ascending=[True, False])

dogs["name"]

new_dogs=dogs[dogs["name"]]

dogs["new_dogs_column"]= new chart

unique_dogs = vet_visits.drop_duplicates(subset=["name", "breed"])-- Drop duplicates

unique_dogs["breed"].value_counts(sort=True, normalize=True)

dogs.groupby(["color", "breed"])["weight_kg"].agg([min, max, sum])

import numpy as np
dogs.pivot_table(values="weight_kg", index="color", columns="breed", fill_value=0, margins=True, aggfunc=np.median)

dogs_ind3.loc[["Labrador", "Chihuahua"]]

dogs_srt.loc["Chow Chow":"Poodle"] --- outer index
dogs_srt.loc[("Labrador", "Brown"):("Schnauzer", "Grey")] --- inner index

dogs_srt.loc[:, "name":"height_cm"]--- slicing columns



---

***Index***
dogs_ind = dogs.set_index("name")
dogs_ind.reset_index(drop=True/False)
dogs_ind3.sort_index(level=["color", "breed"], ascending=[True, False])

---

