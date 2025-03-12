### Q1
``` python
import pandas as pd
df= pd.read_csv('/auto-mpg.csv')
print(df.head(10))
print("total no of roaws and columns ", df.shape)
print(df.describe)
```
### Q2
``` python
df[(df['model year'] == 75) & (df['weight'] < 3000)][['car name', 'weight', 'mpg']]

```

### Q3
``` python
df['horsepower].isna().sum()
```

### Q4
``` python
df.isna().sum()
df['horsepower'].isnull().sum()
df['horsepower'] = pd.to_numeric(df['horsepower'], errors='coerce')
df['weight'] = pd.to_numeric(df['weight'], errors='coerce')
df['power_to_weight_ratio'] = df['horsepower'] / df['weight']
df.head()
```

### Q5
``` python
df.groupby('origin')['mpg'].mean()
```

### Q6
``` python
df.sort_values(by='mpg', ascending=False).head(10)
```

### Q7
``` python
def performance_score(row): 
 return row['mpg'] * row['acceleration'] / row['weight']
df['performance_score'] = df.apply(performance_score, axis=1)
df.head()
```

### Q8
``` python
df.groupby('model year')[['mpg', 'weight', 'horsepower']].mean()
```

### Q9
``` python
df[df['mpg'] > 30][['mpg', 'cylinders', 'horsepower', 'weight']].to_csv('high_mpg_cars.csv', index=False)
dt= pd.read_csv('/content/high_mpg_cars.csv')
```

### Q10
``` python
q1=df['mpg'].quantile(0.25)
q3=df['mpg'].quantile(0.75)
iqr=q3-q1
lb=q1-1.5*iqr
ub=q3+1.5*iqr
odf = df[(df['mpg'] < lb) | (df['mpg'] > ub)][['car name', 'mpg', 'model year']]
print(odf)
```



