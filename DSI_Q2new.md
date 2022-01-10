```python
import pandas as pd
import numpy as np
```

# Q.1


```python
df1=pd.read_csv('data.tsv', sep='\t')
```


```python
df1.head(10)
```





  <div id="df-3faa4b1e-89b3-420e-9232-9e2e7dea4bcd">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tconst</th>
      <th>averageRating</th>
      <th>numVotes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0000001</td>
      <td>5.8</td>
      <td>1422.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt0000002</td>
      <td>6.4</td>
      <td>168.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0000003</td>
      <td>6.6</td>
      <td>1015.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0000004</td>
      <td>6.4</td>
      <td>100.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0000005</td>
      <td>6.2</td>
      <td>1713.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>tt0000006</td>
      <td>5.5</td>
      <td>88.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>tt0000007</td>
      <td>5.5</td>
      <td>573.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>tt0000008</td>
      <td>5.6</td>
      <td>1526.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>tt0000009</td>
      <td>5.5</td>
      <td>70.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>tt0000010</td>
      <td>6.9</td>
      <td>5083.0</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-3faa4b1e-89b3-420e-9232-9e2e7dea4bcd')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-3faa4b1e-89b3-420e-9232-9e2e7dea4bcd button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-3faa4b1e-89b3-420e-9232-9e2e7dea4bcd');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>





```python

df2=pd.read_csv('data-2.tsv', sep='\t')
```


```python
df2.head(10)
```





  <div id="df-8e5c0d22-3bc3-4393-a086-638e81f4c5e7">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>titleId</th>
      <th>ordering</th>
      <th>title</th>
      <th>region</th>
      <th>language</th>
      <th>types</th>
      <th>attributes</th>
      <th>isOriginalTitle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0000001</td>
      <td>1</td>
      <td>Carmencita - spanyol tánc</td>
      <td>HU</td>
      <td>\N</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt0000001</td>
      <td>2</td>
      <td>Карменсита</td>
      <td>RU</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0000001</td>
      <td>3</td>
      <td>Carmencita</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0000001</td>
      <td>4</td>
      <td>Carmencita</td>
      <td>\N</td>
      <td>\N</td>
      <td>original</td>
      <td>\N</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0000002</td>
      <td>1</td>
      <td>Le clown et ses chiens</td>
      <td>\N</td>
      <td>\N</td>
      <td>original</td>
      <td>\N</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>5</th>
      <td>tt0000002</td>
      <td>2</td>
      <td>A bohóc és kutyái</td>
      <td>HU</td>
      <td>\N</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>6</th>
      <td>tt0000002</td>
      <td>3</td>
      <td>Le clown et ses chiens</td>
      <td>FR</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>7</th>
      <td>tt0000002</td>
      <td>4</td>
      <td>Clovnul si cainii sai</td>
      <td>RO</td>
      <td>\N</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>8</th>
      <td>tt0000002</td>
      <td>5</td>
      <td>The Clown and His Dogs</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>literal English title</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>9</th>
      <td>tt0000002</td>
      <td>6</td>
      <td>Клоун и его собаки</td>
      <td>RU</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-8e5c0d22-3bc3-4393-a086-638e81f4c5e7')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-8e5c0d22-3bc3-4393-a086-638e81f4c5e7 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-8e5c0d22-3bc3-4393-a086-638e81f4c5e7');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>





```python
df3=pd.read_csv('data-3.tsv', sep='\t')
```


```python
df3.head(10)
```





  <div id="df-f5b10315-59e1-484e-a7b0-e8a766038f25">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tconst</th>
      <th>titleType</th>
      <th>primaryTitle</th>
      <th>originalTitle</th>
      <th>isAdult</th>
      <th>startYear</th>
      <th>endYear</th>
      <th>runtimeMinutes</th>
      <th>genres</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0000001</td>
      <td>short</td>
      <td>Carmencita</td>
      <td>Carmencita</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt0000002</td>
      <td>short</td>
      <td>Le clown et ses chiens</td>
      <td>Le clown et ses chiens</td>
      <td>0.0</td>
      <td>1892.0</td>
      <td>\N</td>
      <td>5</td>
      <td>Animation,Short</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0000003</td>
      <td>short</td>
      <td>Pauvre Pierrot</td>
      <td>Pauvre Pierrot</td>
      <td>0.0</td>
      <td>1892.0</td>
      <td>\N</td>
      <td>4</td>
      <td>Animation,Comedy,Romance</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0000004</td>
      <td>short</td>
      <td>Un bon bock</td>
      <td>Un bon bock</td>
      <td>0.0</td>
      <td>1892.0</td>
      <td>\N</td>
      <td>\N</td>
      <td>Animation,Short</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0000005</td>
      <td>short</td>
      <td>Blacksmith Scene</td>
      <td>Blacksmith Scene</td>
      <td>0.0</td>
      <td>1893.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Comedy,Short</td>
    </tr>
    <tr>
      <th>5</th>
      <td>tt0000006</td>
      <td>short</td>
      <td>Chinese Opium Den</td>
      <td>Chinese Opium Den</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Short</td>
    </tr>
    <tr>
      <th>6</th>
      <td>tt0000007</td>
      <td>short</td>
      <td>Corbett and Courtney Before the Kinetograph</td>
      <td>Corbett and Courtney Before the Kinetograph</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Short,Sport</td>
    </tr>
    <tr>
      <th>7</th>
      <td>tt0000008</td>
      <td>short</td>
      <td>Edison Kinetoscopic Record of a Sneeze</td>
      <td>Edison Kinetoscopic Record of a Sneeze</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>8</th>
      <td>tt0000009</td>
      <td>movie</td>
      <td>Miss Jerry</td>
      <td>Miss Jerry</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>45</td>
      <td>Romance</td>
    </tr>
    <tr>
      <th>9</th>
      <td>tt0000010</td>
      <td>short</td>
      <td>Employees Leaving the Lumière Factory</td>
      <td>La sortie de l'usine Lumière à Lyon</td>
      <td>0.0</td>
      <td>1895.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-f5b10315-59e1-484e-a7b0-e8a766038f25')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-f5b10315-59e1-484e-a7b0-e8a766038f25 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-f5b10315-59e1-484e-a7b0-e8a766038f25');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>




# Q.2


```python
duplicate=df1[df1.duplicated()]
print(duplicate)
```

    Empty DataFrame
    Columns: [tconst, averageRating, numVotes]
    Index: []



```python
duplicate=df2[df2.duplicated()]
print(duplicate)
```

    Empty DataFrame
    Columns: [titleId, ordering, title, region, language, types, attributes, isOriginalTitle]
    Index: []



```python
duplicate=df3[df3.duplicated()]
print(duplicate)
```

    Empty DataFrame
    Columns: [tconst, titleType, primaryTitle, originalTitle, isAdult, startYear, endYear, runtimeMinutes, genres]
    Index: []



```python
df1.duplicated().sum()
```




    0




```python
df2.duplicated().sum()
```




    0




```python
df3.duplicated().sum()
```




    0




```python
df2.rename(columns = {'titleId':'tconst'}, inplace = True)
```


```python
df2.head()
```





  <div id="df-bdf1fe7e-f319-44e9-9425-604a903ff749">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tconst</th>
      <th>ordering</th>
      <th>title</th>
      <th>region</th>
      <th>language</th>
      <th>types</th>
      <th>attributes</th>
      <th>isOriginalTitle</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0000001</td>
      <td>1</td>
      <td>Carmencita - spanyol tánc</td>
      <td>HU</td>
      <td>\N</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt0000001</td>
      <td>2</td>
      <td>Карменсита</td>
      <td>RU</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0000001</td>
      <td>3</td>
      <td>Carmencita</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0000001</td>
      <td>4</td>
      <td>Carmencita</td>
      <td>\N</td>
      <td>\N</td>
      <td>original</td>
      <td>\N</td>
      <td>1.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0000002</td>
      <td>1</td>
      <td>Le clown et ses chiens</td>
      <td>\N</td>
      <td>\N</td>
      <td>original</td>
      <td>\N</td>
      <td>1.0</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-bdf1fe7e-f319-44e9-9425-604a903ff749')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-bdf1fe7e-f319-44e9-9425-604a903ff749 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-bdf1fe7e-f319-44e9-9425-604a903ff749');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>




# Q.3


```python
#Inner Join
merged_df = pd.merge(pd.merge(df1,df2,on='tconst'),df3,on='tconst')
```


```python
merged_df.head()
```





  <div id="df-39a08461-ebc2-4bc4-9388-42511f480d6f">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tconst</th>
      <th>averageRating</th>
      <th>numVotes</th>
      <th>ordering</th>
      <th>title</th>
      <th>region</th>
      <th>language</th>
      <th>types</th>
      <th>attributes</th>
      <th>isOriginalTitle</th>
      <th>titleType</th>
      <th>primaryTitle</th>
      <th>originalTitle</th>
      <th>isAdult</th>
      <th>startYear</th>
      <th>endYear</th>
      <th>runtimeMinutes</th>
      <th>genres</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>tt0000001</td>
      <td>5.8</td>
      <td>1422.0</td>
      <td>1</td>
      <td>Carmencita - spanyol tánc</td>
      <td>HU</td>
      <td>\N</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>Carmencita</td>
      <td>Carmencita</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>1</th>
      <td>tt0000001</td>
      <td>5.8</td>
      <td>1422.0</td>
      <td>2</td>
      <td>Карменсита</td>
      <td>RU</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>Carmencita</td>
      <td>Carmencita</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>2</th>
      <td>tt0000001</td>
      <td>5.8</td>
      <td>1422.0</td>
      <td>3</td>
      <td>Carmencita</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>Carmencita</td>
      <td>Carmencita</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>3</th>
      <td>tt0000001</td>
      <td>5.8</td>
      <td>1422.0</td>
      <td>4</td>
      <td>Carmencita</td>
      <td>\N</td>
      <td>\N</td>
      <td>original</td>
      <td>\N</td>
      <td>1.0</td>
      <td>short</td>
      <td>Carmencita</td>
      <td>Carmencita</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>4</th>
      <td>tt0000002</td>
      <td>6.4</td>
      <td>168.0</td>
      <td>1</td>
      <td>Le clown et ses chiens</td>
      <td>\N</td>
      <td>\N</td>
      <td>original</td>
      <td>\N</td>
      <td>1.0</td>
      <td>short</td>
      <td>Le clown et ses chiens</td>
      <td>Le clown et ses chiens</td>
      <td>0.0</td>
      <td>1892.0</td>
      <td>\N</td>
      <td>5</td>
      <td>Animation,Short</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-39a08461-ebc2-4bc4-9388-42511f480d6f')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-39a08461-ebc2-4bc4-9388-42511f480d6f button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-39a08461-ebc2-4bc4-9388-42511f480d6f');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>





```python
len(merged_df)
```




    17564




```python
merged_df['titleType'].unique()
```




    array(['short', 'movie'], dtype=object)




```python
merged_df['titleType'].nunique()
```




    2



# Q.4


```python
df_new = merged_df[(merged_df['language'] == 'en') | (merged_df['region'] == 'US') & (merged_df['titleType']== 'movie') ]
```

# Q.5


```python
df_new.head()
```





  <div id="df-315e0cdd-e052-4683-a0e3-9d23e922cd8c">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tconst</th>
      <th>averageRating</th>
      <th>numVotes</th>
      <th>ordering</th>
      <th>title</th>
      <th>region</th>
      <th>language</th>
      <th>types</th>
      <th>attributes</th>
      <th>isOriginalTitle</th>
      <th>titleType</th>
      <th>primaryTitle</th>
      <th>originalTitle</th>
      <th>isAdult</th>
      <th>startYear</th>
      <th>endYear</th>
      <th>runtimeMinutes</th>
      <th>genres</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>51</th>
      <td>tt0000009</td>
      <td>5.5</td>
      <td>70.0</td>
      <td>3</td>
      <td>Miss Jerry</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>Miss Jerry</td>
      <td>Miss Jerry</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>45</td>
      <td>Romance</td>
    </tr>
    <tr>
      <th>74</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>11</td>
      <td>The Arrival of a Train</td>
      <td>XWW</td>
      <td>en</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>76</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>13</td>
      <td>The Arrival of a Train at La Ciotat</td>
      <td>XWW</td>
      <td>en</td>
      <td>alternative</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>85</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>21</td>
      <td>The Arrival of a Train</td>
      <td>XEU</td>
      <td>en</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
    <tr>
      <th>131</th>
      <td>tt0000016</td>
      <td>5.9</td>
      <td>967.0</td>
      <td>1</td>
      <td>Boat Leaving the Port</td>
      <td>XWW</td>
      <td>en</td>
      <td>\N</td>
      <td>informal title</td>
      <td>0.0</td>
      <td>short</td>
      <td>Barque sortant du port</td>
      <td>Barque sortant du port</td>
      <td>0.0</td>
      <td>1895.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-315e0cdd-e052-4683-a0e3-9d23e922cd8c')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-315e0cdd-e052-4683-a0e3-9d23e922cd8c button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-315e0cdd-e052-4683-a0e3-9d23e922cd8c');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>





```python
df_new.loc[df_new['log10Votes'] == np.log10(df_new['numVotes'])]
```





  <div id="df-3f602583-96b8-4b59-a9f8-7a7cbc356cd1">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tconst</th>
      <th>averageRating</th>
      <th>numVotes</th>
      <th>ordering</th>
      <th>title</th>
      <th>region</th>
      <th>language</th>
      <th>types</th>
      <th>attributes</th>
      <th>isOriginalTitle</th>
      <th>titleType</th>
      <th>primaryTitle</th>
      <th>originalTitle</th>
      <th>isAdult</th>
      <th>startYear</th>
      <th>endYear</th>
      <th>runtimeMinutes</th>
      <th>genres</th>
      <th>log10Votes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>51</th>
      <td>tt0000009</td>
      <td>5.5</td>
      <td>70.0</td>
      <td>3</td>
      <td>Miss Jerry</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>Miss Jerry</td>
      <td>Miss Jerry</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>45</td>
      <td>Romance</td>
      <td>1.845098</td>
    </tr>
    <tr>
      <th>74</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>11</td>
      <td>The Arrival of a Train</td>
      <td>XWW</td>
      <td>en</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
      <td>3.929879</td>
    </tr>
    <tr>
      <th>76</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>13</td>
      <td>The Arrival of a Train at La Ciotat</td>
      <td>XWW</td>
      <td>en</td>
      <td>alternative</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
      <td>3.929879</td>
    </tr>
    <tr>
      <th>85</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>21</td>
      <td>The Arrival of a Train</td>
      <td>XEU</td>
      <td>en</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
      <td>3.929879</td>
    </tr>
    <tr>
      <th>131</th>
      <td>tt0000016</td>
      <td>5.9</td>
      <td>967.0</td>
      <td>1</td>
      <td>Boat Leaving the Port</td>
      <td>XWW</td>
      <td>en</td>
      <td>\N</td>
      <td>informal title</td>
      <td>0.0</td>
      <td>short</td>
      <td>Barque sortant du port</td>
      <td>Barque sortant du port</td>
      <td>0.0</td>
      <td>1895.0</td>
      <td>\N</td>
      <td>1</td>
      <td>Documentary,Short</td>
      <td>2.985426</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>17546</th>
      <td>tt0016130</td>
      <td>7.8</td>
      <td>5.0</td>
      <td>2</td>
      <td>No Fight Without Money</td>
      <td>XWW</td>
      <td>en</td>
      <td>alternative</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>Musen Fusen Uchien Puchan</td>
      <td>Musen Fusen Uchien Puchan</td>
      <td>0.0</td>
      <td>1925.0</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.698970</td>
    </tr>
    <tr>
      <th>17547</th>
      <td>tt0016130</td>
      <td>7.8</td>
      <td>5.0</td>
      <td>3</td>
      <td>No Money, No War</td>
      <td>XWW</td>
      <td>en</td>
      <td>alternative</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>Musen Fusen Uchien Puchan</td>
      <td>Musen Fusen Uchien Puchan</td>
      <td>0.0</td>
      <td>1925.0</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.698970</td>
    </tr>
    <tr>
      <th>17550</th>
      <td>tt0016130</td>
      <td>7.8</td>
      <td>5.0</td>
      <td>6</td>
      <td>No Money, No Fight</td>
      <td>XWW</td>
      <td>en</td>
      <td>alternative</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>Musen Fusen Uchien Puchan</td>
      <td>Musen Fusen Uchien Puchan</td>
      <td>0.0</td>
      <td>1925.0</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.698970</td>
    </tr>
    <tr>
      <th>17554</th>
      <td>tt0016134</td>
      <td>7.7</td>
      <td>6.0</td>
      <td>1</td>
      <td>My Lady's Lips</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>My Lady's Lips</td>
      <td>My Lady's Lips</td>
      <td>0.0</td>
      <td>1925.0</td>
      <td>\N</td>
      <td>70</td>
      <td>Crime,Drama</td>
      <td>0.778151</td>
    </tr>
    <tr>
      <th>17561</th>
      <td>tt0016142</td>
      <td>6.8</td>
      <td>85.0</td>
      <td>5</td>
      <td>The Mystic</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>The Mystic</td>
      <td>The Mystic</td>
      <td>0.0</td>
      <td>1925.0</td>
      <td>\N</td>
      <td>70</td>
      <td>Drama</td>
      <td>1.929419</td>
    </tr>
  </tbody>
</table>
<p>2057 rows × 19 columns</p>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-3f602583-96b8-4b59-a9f8-7a7cbc356cd1')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-3f602583-96b8-4b59-a9f8-7a7cbc356cd1 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-3f602583-96b8-4b59-a9f8-7a7cbc356cd1');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>




# Q.6


```python
df_new['genres']=df_new['genres'].str.lower()
```

    /usr/local/lib/python3.7/dist-packages/ipykernel_launcher.py:1: SettingWithCopyWarning: 
    A value is trying to be set on a copy of a slice from a DataFrame.
    Try using .loc[row_indexer,col_indexer] = value instead
    
    See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
      """Entry point for launching an IPython kernel.



```python
df_new.head()
```





  <div id="df-4ea4c028-d82f-4838-a5da-9bfc38a87747">
    <div class="colab-df-container">
      <div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>tconst</th>
      <th>averageRating</th>
      <th>numVotes</th>
      <th>ordering</th>
      <th>title</th>
      <th>region</th>
      <th>language</th>
      <th>types</th>
      <th>attributes</th>
      <th>isOriginalTitle</th>
      <th>titleType</th>
      <th>primaryTitle</th>
      <th>originalTitle</th>
      <th>isAdult</th>
      <th>startYear</th>
      <th>endYear</th>
      <th>runtimeMinutes</th>
      <th>genres</th>
      <th>log10Votes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>51</th>
      <td>tt0000009</td>
      <td>5.5</td>
      <td>70.0</td>
      <td>3</td>
      <td>Miss Jerry</td>
      <td>US</td>
      <td>\N</td>
      <td>\N</td>
      <td>\N</td>
      <td>0.0</td>
      <td>movie</td>
      <td>Miss Jerry</td>
      <td>Miss Jerry</td>
      <td>0.0</td>
      <td>1894.0</td>
      <td>\N</td>
      <td>45</td>
      <td>romance</td>
      <td>1.845098</td>
    </tr>
    <tr>
      <th>74</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>11</td>
      <td>The Arrival of a Train</td>
      <td>XWW</td>
      <td>en</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>documentary,short</td>
      <td>3.929879</td>
    </tr>
    <tr>
      <th>76</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>13</td>
      <td>The Arrival of a Train at La Ciotat</td>
      <td>XWW</td>
      <td>en</td>
      <td>alternative</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>documentary,short</td>
      <td>3.929879</td>
    </tr>
    <tr>
      <th>85</th>
      <td>tt0000012</td>
      <td>7.4</td>
      <td>8509.0</td>
      <td>21</td>
      <td>The Arrival of a Train</td>
      <td>XEU</td>
      <td>en</td>
      <td>imdbDisplay</td>
      <td>\N</td>
      <td>0.0</td>
      <td>short</td>
      <td>The Arrival of a Train</td>
      <td>L'arrivée d'un train à La Ciotat</td>
      <td>0.0</td>
      <td>1896.0</td>
      <td>\N</td>
      <td>1</td>
      <td>documentary,short</td>
      <td>3.929879</td>
    </tr>
    <tr>
      <th>131</th>
      <td>tt0000016</td>
      <td>5.9</td>
      <td>967.0</td>
      <td>1</td>
      <td>Boat Leaving the Port</td>
      <td>XWW</td>
      <td>en</td>
      <td>\N</td>
      <td>informal title</td>
      <td>0.0</td>
      <td>short</td>
      <td>Barque sortant du port</td>
      <td>Barque sortant du port</td>
      <td>0.0</td>
      <td>1895.0</td>
      <td>\N</td>
      <td>1</td>
      <td>documentary,short</td>
      <td>2.985426</td>
    </tr>
  </tbody>
</table>
</div>
      <button class="colab-df-convert" onclick="convertToInteractive('df-4ea4c028-d82f-4838-a5da-9bfc38a87747')"
              title="Convert this dataframe to an interactive table."
              style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px"viewBox="0 0 24 24"
       width="24px">
    <path d="M0 0h24v24H0V0z" fill="none"/>
    <path d="M18.56 5.44l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94zm-11 1L8.5 8.5l.94-2.06 2.06-.94-2.06-.94L8.5 2.5l-.94 2.06-2.06.94zm10 10l.94 2.06.94-2.06 2.06-.94-2.06-.94-.94-2.06-.94 2.06-2.06.94z"/><path d="M17.41 7.96l-1.37-1.37c-.4-.4-.92-.59-1.43-.59-.52 0-1.04.2-1.43.59L10.3 9.45l-7.72 7.72c-.78.78-.78 2.05 0 2.83L4 21.41c.39.39.9.59 1.41.59.51 0 1.02-.2 1.41-.59l7.78-7.78 2.81-2.81c.8-.78.8-2.07 0-2.86zM5.41 20L4 18.59l7.72-7.72 1.47 1.35L5.41 20z"/>
  </svg>
      </button>

  <style>
    .colab-df-container {
      display:flex;
      flex-wrap:wrap;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

      <script>
        const buttonEl =
          document.querySelector('#df-4ea4c028-d82f-4838-a5da-9bfc38a87747 button.colab-df-convert');
        buttonEl.style.display =
          google.colab.kernel.accessAllowed ? 'block' : 'none';

        async function convertToInteractive(key) {
          const element = document.querySelector('#df-4ea4c028-d82f-4838-a5da-9bfc38a87747');
          const dataTable =
            await google.colab.kernel.invokeFunction('convertToInteractive',
                                                     [key], {});
          if (!dataTable) return;

          const docLinkHtml = 'Like what you see? Visit the ' +
            '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
            + ' to learn more about interactive tables.';
          element.innerHTML = '';
          dataTable['output_type'] = 'display_data';
          await google.colab.output.renderOutput(dataTable, element);
          const docLink = document.createElement('div');
          docLink.innerHTML = docLinkHtml;
          element.appendChild(docLink);
        }
      </script>
    </div>
  </div>





```python
df_new.groupby('genres')['log10Votes'].mean().nlargest(10)
```




    genres
    documentary,fantasy,horror     3.982135
    fantasy,horror,mystery         3.976099
    comedy,romance,thriller        3.942504
    fantasy,horror                 3.909337
    drama,thriller,western         3.904932
    comedy,drama,family            3.859733
    crime,mystery,thriller         3.794349
    comedy,war                     3.690728
    adventure,fantasy,sci-fi       3.671516
    adventure,animation,fantasy    3.648262
    Name: log10Votes, dtype: float64




```python
df_new.groupby('genres')['averageRating'].mean().nlargest(10)
```




    genres
    action,comedy,sport            8.3
    adventure,fantasy,romance      7.9
    comedy,romance,thriller        7.9
    crime,mystery,thriller         7.9
    drama,romance,thriller         7.9
    drama,thriller,western         7.9
    adventure,animation,fantasy    7.8
    animation,comedy,short         7.8
    documentary,fantasy,horror     7.7
    drama,fantasy,thriller         7.7
    Name: averageRating, dtype: float64



## Q.7


```python
df_new.groupby('averageRating')
df_new.plot.scatter(x='averageRating', y='log10Votes')
```

## Q.8


```python
import seaborn as sns
import matplotlib.pyplot as plt
%matplotlib inline
```


```python
X = df_new.iloc[:, 1].values.reshape(-1, 1)
y = df_new.iloc[:, -1].values.reshape(-1, 1)
```


```python
print(X)
```


```python
print(y)
```


```python
from sklearn.model_selection import train_test_split
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size = 0.2, random_state = 0)
```


```python
from sklearn.linear_model import LinearRegression
regressor = LinearRegression()
regressor.fit(X_train, y_train)
```




    LinearRegression()




```python
y_pred = regressor.predict(X_test)
```


```python
plt.scatter(X_train, y_train, color = 'red')
plt.plot(X_train, regressor.predict(X_train), color='blue')
plt.title('averageRating vs log10Votes (Training Set)')
plt.xlabel('averageRating')
plt.ylabel('log10Votes')
plt.show()
```


```python
plt.scatter(X_test, y_test, color = 'red')
plt.plot(X_train, regressor.predict(X_train), color='blue')
plt.title('averageRating vs log10Votes (Test Set)')
plt.xlabel('averageRating')
plt.ylabel('log10Votes')
plt.show()
```


    
![png](output_44_0.png)
    



```python
print(regressor.intercept_)
print(regressor.coef_)
```

    [0.00222876]
    [[0.25195654]]


Linear Regression Using Scipy


```python
from scipy import stats
from scipy.stats import linregress

```


```python

```


```python

```

Linear Regression using Pytorch


```python
import torch
import torch.nn as nn
from torch.autograd import Variable
```


```python
x_values = df_new.iloc[:, 1].values
x_train = np.array(x_values, dtype=np.float32)
x_train = x_train.reshape(-1, 1)
```


```python
y_values = df_new.iloc[:, -1].values
y_train = np.array(y_values, dtype=np.float32)
y_train = y_train.reshape(-1, 1)
```


```python
class linearRegression(torch.nn.Module):
    def __init__(self, inputSize, outputSize):
        super(linearRegression, self).__init__()
        self.linear = torch.nn.Linear(inputSize, outputSize)

    def forward(self, x):
        out = self.linear(x)
        return out
```


```python
inputDim = 1        
outputDim = 1       
learningRate = 0.01 
epochs = 100

model = linearRegression(inputDim, outputDim)
if torch.cuda.is_available():
    model.cuda()
```


```python
criterion = torch.nn.MSELoss() 
optimizer = torch.optim.SGD(model.parameters(), lr=learningRate)
```


```python
for epoch in range(epochs):
    # Converting inputs and labels to Variable
    if torch.cuda.is_available():
        inputs = Variable(torch.from_numpy(x_train).cuda())
        labels = Variable(torch.from_numpy(y_train).cuda())
    else:
        inputs = Variable(torch.from_numpy(x_train))
        labels = Variable(torch.from_numpy(y_train))

    optimizer.zero_grad()

    outputs = model(inputs)

    loss = criterion(outputs, labels)
    print(loss)
    loss.backward()

    optimizer.step()

    print('epoch {}, loss {}'.format(epoch, loss.item()))
```

    tensor(3.6778, grad_fn=<MseLossBackward0>)
    epoch 0, loss 3.6777961254119873
    tensor(0.7677, grad_fn=<MseLossBackward0>)
    epoch 1, loss 0.7677470445632935
    tensor(0.7232, grad_fn=<MseLossBackward0>)
    epoch 2, loss 0.723159670829773
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 3, loss 0.7224764823913574
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 4, loss 0.722465991973877
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 5, loss 0.7224658131599426
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 6, loss 0.7224657535552979
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 7, loss 0.7224657535552979
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 8, loss 0.7224657535552979
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 9, loss 0.7224656939506531
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 10, loss 0.7224656939506531
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 11, loss 0.7224656939506531
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 12, loss 0.7224656939506531
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 13, loss 0.7224656343460083
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 14, loss 0.7224656343460083
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 15, loss 0.7224655747413635
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 16, loss 0.7224655747413635
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 17, loss 0.7224655151367188
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 18, loss 0.7224655151367188
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 19, loss 0.7224655151367188
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 20, loss 0.7224653959274292
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 21, loss 0.7224653959274292
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 22, loss 0.7224653959274292
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 23, loss 0.722465455532074
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 24, loss 0.7224653959274292
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 25, loss 0.7224653959274292
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 26, loss 0.7224652767181396
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 27, loss 0.7224653363227844
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 28, loss 0.7224652171134949
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 29, loss 0.7224652767181396
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 30, loss 0.7224652171134949
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 31, loss 0.7224652171134949
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 32, loss 0.7224651575088501
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 33, loss 0.7224651575088501
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 34, loss 0.7224650979042053
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 35, loss 0.7224651575088501
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 36, loss 0.7224650979042053
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 37, loss 0.7224650382995605
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 38, loss 0.7224649786949158
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 39, loss 0.7224650382995605
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 40, loss 0.7224650382995605
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 41, loss 0.7224650382995605
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 42, loss 0.722464919090271
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 43, loss 0.722464919090271
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 44, loss 0.722464919090271
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 45, loss 0.722464919090271
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 46, loss 0.722464919090271
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 47, loss 0.7224647998809814
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 48, loss 0.7224647998809814
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 49, loss 0.7224647998809814
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 50, loss 0.7224647998809814
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 51, loss 0.7224646806716919
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 52, loss 0.7224647402763367
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 53, loss 0.7224647402763367
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 54, loss 0.7224646806716919
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 55, loss 0.7224646806716919
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 56, loss 0.7224646210670471
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 57, loss 0.7224645614624023
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 58, loss 0.7224645614624023
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 59, loss 0.7224646210670471
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 60, loss 0.7224644422531128
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 61, loss 0.7224645614624023
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 62, loss 0.7224645614624023
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 63, loss 0.7224645018577576
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 64, loss 0.7224644422531128
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 65, loss 0.722464382648468
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 66, loss 0.7224644422531128
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 67, loss 0.7224644422531128
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 68, loss 0.722464382648468
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 69, loss 0.722464382648468
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 70, loss 0.7224643230438232
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 71, loss 0.7224643230438232
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 72, loss 0.7224642634391785
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 73, loss 0.7224642634391785
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 74, loss 0.7224642038345337
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 75, loss 0.7224642038345337
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 76, loss 0.7224642038345337
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 77, loss 0.7224640846252441
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 78, loss 0.7224641442298889
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 79, loss 0.7224640846252441
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 80, loss 0.7224640846252441
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 81, loss 0.7224640846252441
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 82, loss 0.7224640250205994
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 83, loss 0.7224640250205994
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 84, loss 0.7224640250205994
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 85, loss 0.7224640250205994
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 86, loss 0.7224640250205994
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 87, loss 0.7224639058113098
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 88, loss 0.7224639654159546
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 89, loss 0.722463846206665
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 90, loss 0.7224639058113098
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 91, loss 0.7224639058113098
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 92, loss 0.722463846206665
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 93, loss 0.722463846206665
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 94, loss 0.722463846206665
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 95, loss 0.7224637866020203
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 96, loss 0.7224637269973755
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 97, loss 0.7224637269973755
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 98, loss 0.7224637269973755
    tensor(0.7225, grad_fn=<MseLossBackward0>)
    epoch 99, loss 0.7224637269973755



```python
with torch.no_grad(): # we don't need gradients in the testing phase
    if torch.cuda.is_available():
        predicted = model(Variable(torch.from_numpy(x_train).cuda())).cpu().data.numpy()
    else:
        predicted = model(Variable(torch.from_numpy(x_train))).data.numpy()
    print(predicted)

plt.clf()
plt.plot(x_train, y_train, 'go', label='True data', alpha=0.5)
plt.plot(x_train, predicted, '--', label='Predictions', alpha=0.5)
plt.legend(loc='best')
plt.show()
```

    [[1.3852675]
     [1.8800396]
     [1.8800396]
     ...
     [1.9842023]
     [1.9581615]
     [1.7237958]]



    
![png](output_58_1.png)
    

