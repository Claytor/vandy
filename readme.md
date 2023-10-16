Instructions:
Using any platform you would like (Google Sheets, Slides, PowerBI, Tableau etc.) create a dashboard report displaying the following prompts.  Be prepared to walk through the dashboard explaining what conclusions you came to from analyzing the prompts, what data cleaning steps you took, as well as using visualizations and why you chose them.

The audience is a non-technical academic board that oversees the departments annotated in the data.  You will have 25 minute time cap to present.

1) **Salary Expectations:**
   1) [ ] Show Median and Average Salary expectations by department
      1) [ ] How is sallary related to degree satisfaction?
      2) [ ] How is sallary related to persuing a degree in the field?
2) **Degree Satisfaction by Department:**
   1) [ ] Display the distribution of 'Do you like your degree?' across different departments
3) **Hobbies and Part-time Jobs:**
   1) [ ] Visualize the percentage of candidates with a 'part-time job' based on their hobbies
      1) [ ] Are Hobbies related to degree satisfaction
      2) [ ] Are Hobbies related to seeking
4) **Financial Status and Part-time Jobs:**
   1) [ ] Display the distribution of 'Financial Status' and the percentage of candidates with a 'part-time job'
      1) [ ] Does
5) **Degree Satisfaction:**
   1) [ ] Show the percentage of candidates who like their degree and are willing to pursue a career based on their degree
6) **Department-wise Analysis:**
   1) [ ] Compare the average '10th Mark', '12th Mark', and 'college mark' for different departments

***BONUS
**Supplementing the provided prompts, include any additional charts or visualizations that shed light on their  likelyhood to persue a degree in thier career and their level of satisfaction with the chosen degree

Overall graph should be bigger. 1 facet for each department

- hypothesis
   - if you are more happy with your degree then you are more likely to seek out a position within the area of your degree?
** - Recreate #5 faceted by department** 
      - Do only for neutral, willing, and eager
      - Same axis for all facets
      - Be careful about the axis

# Saving figure as html
fig_happy_likely_1.write_html('../dashboard/plotly_html/q5_happy_likely_1.html')


# Creating a grouped bar chart
fig_happy_likely_1 = px.bar(happy_likely_neutral, x='percentage', y='degree_happy',
             color='career_in_degree',
             title="Degree Happiness and Career Pursuit",
             labels={'percentage': 'Percent',
                     'career_in_degree': 'Career in Degree',
                     'degree_happy': 'Happy With Degree'},
             barmode='relative')
happy_likely_order = ['No', 'Yes']
# Update layout and labels
fig_happy_likely_1.update_layout(xaxis_title='Percent',
                  yaxis_title='Degree Satisfaction',
                  legend_title='Career in Degree',
                  paper_bgcolor='rgba(0,0,0,0)',
                  plot_bgcolor='rgba(0,0,0,0)',
                  title={'y':0.95,
                         'x':0.5,
                         'xanchor': 'center',
                         'yanchor': 'top'},
                  yaxis=dict(categoryorder='array',    
                             categoryarray=happy_likely_order))
fig_happy_likely_1.show()

# Saving figure as html
fig_happy_likely_1.write_html('../dashboard/plotly_html/q5_happy_likely_1.html')


color_map = {
    'Category1': '#ff0000',  # red
    'Category3': '#0000ff',  # blue
    'Category1': '#ff0000',  # red
}


paper_bg='rgba(0,0,0,0)'
plot_bg='rgba(0,0,0,0)