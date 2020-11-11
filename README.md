# Visual Research Paper
### Project for IntraMIC Hack 'September 2020
<hr>

## Research Papers are Boring!
    
   ### Objective: 

   Take a pdf of a research paper and generate a comprehensive mind map as a means of visual summarization. 
   
   ### Motivation:
   
   As executives in an undergraduate machine intelligence research community, we saw a need in fellow students with learning disabilities who had difficulty  understanding the often tedious text of research papers. This project also proved to be extremely helpful for visual learners within the community as well. We’re hoping to make this tool open to the general public soon.
   
   ### How It Works:
   
   ![](beryllium1.gif)
   
   ### Components:
   1. Extract the structured text from the pdf
        ##### Input: PDF
        1. Extract text itself
        2. Identify headings and subheadings
        ##### Output_1: The outline of the document in two parts: 1. List of Headings 2. List of Dicts Holding Structured Plain Text
   2. Summarization of the lowest levels of content (for now: paragraph)
        ##### Input: Output_1
        1. Using outline, extract paragraph content under each heading
        2. Use summarizer to summarize paragraphs under one heading as one.
            1. Set limit to how many words regardless of number of paragraphs
            2. If the introductory paragraph falls under a heading with no other subheading attached, include summary with heading node.
        3. Update heading line by appending summary 
        4. Replace content in Output_1
        ##### Output_2: Outline with Summarized Paragraphs
   3. Feed Output_2 into application that will generate interactive mind map 
        ##### Input: Output_2 
        1. Generate the interactive mind map by creating a graph using PyVis
        ##### Output_3: Interactive Mind Map = Visual Research Paper
        
   ### To Do:
   1. Extract figures and tables to add its labels to image nodes containing figure/table
   2. Extract formulas to add as separate nodes
   3. Generate a cleaner mind map 
   
   ![](beryllium.gif)

