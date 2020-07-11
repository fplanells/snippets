# Import altair
 import altair as alt 


# Histogram

 
alt.Chart(df).mark_bar().encode(
    x=alt.X('Brain Weight',bin=True,title="Brain Weight Binned"),
    y="count()"
   ).properties(
    width=200,
    height=200,
    title="Histogram of Brain Weight"
)


# Scatter Plot

 
scatter = alt.Chart(df).mark_circle().encode(
    x="Body Weight",
    y="Brain Weight"
)


# Bar Chart

 
trends_bar=alt.Chart(trends).mark_bar().encode(
    x="search_term",
    y="sum(value)",
    color="search_term"
)
