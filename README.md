# CMPE256-FitRec
Term project for CMPE 256.

# Datasets:

[Cleaned Dataset](https://www.kaggle.com/datasets/pypiahmad/endomondo-fitness-trajectories?resource=download)

[Original Website](https://cseweb.ucsd.edu/~jmcauley/datasets/fitrec.html)

`endomondoMeta.json` cannot be read by PySpark due to formatting error. We need to do 2 things to fix:

1. Replace single quote `'` with double quote `"`.

2. Replace the word `None` with `"None"`.

Example fix with `sed`:

```
sed -i '' -e "s/'/\"/g" endomondoMeta.json
sed -i '' -e "s/None/\"None\"/g" endomondoMeta.json
```


# Project Structure

Put your `.json` files inside `data` folder to be ignored during commits.
