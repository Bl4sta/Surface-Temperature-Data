if df_Temp is not None:
    
  df_Temp['']= pd.to_datetime(df_Temp['dt'])
  df_Temp['Year'] = df_Temp['dt'].dt.year
  del df_Temp['dt']

  df_Temp = df_Temp.groupby(['Country', 'Year'])['AverageTemperature'].mean().reset_index()
  df_Temp = df_Temp[df_Temp["Year"] == 2013]**
