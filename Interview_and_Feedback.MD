Prompt:
Create a one-page interview plan + scoring rubric for a Big Data candidate based on the CV below.

- Style & constraints
- Plain English, short, active voice.
- Output as a single page with clear section headers and bullet points.
- Assume a 60-minute interview.
- Focus on Spark, Scala/Java, Kubernetes, data lakehouse (Iceberg/Delta/Hudi), streaming (Kafka), SQL, performance tuning, reliability/observability, and stakeholder skills.

Deliver:
- Role Hypothesis (2–3 lines)
- Risk Areas to Probe (5–8 bullets)
- Interview Plan (60 min) – minute-by-minute blocks with goals
- Core Questions – 8–12 targeted questions mapped to risks
- Hands-on/Whiteboard Task – 1 practical task + success criteria
- Scoring Rubric (100 pts) – categories, weights, what “Strong/OK/Weak” looks like
- Red Flags / Green Signals – 3–5 each
- Follow-ups if time permits – 3 bullets

CV:
[PASTE CV HERE]

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Potential questions:

- spark.read.parquet("hdfs://input_path").filter($"id".isNotNull).write.parquet("hdfs://output_path") 
- Have you ever worked on a project where another team had key information but wasn’t responsive or cooperative? 
- Have you ever started a task or project where the requirements weren’t clear? 
- Have you worked on a project where different stakeholders had conflicting goals or expectations?

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
*"Act as a Big Data interviewer… analyze a CV, conduct an interview, and make a final report about the candidate.

I have unstructured notes on the candidate's responses. I need to generate a structured interview summary based on my notes. Interview summary feedback need for delivery manager and HR for decision making about the candidate. If You need some more information ask me.

Here is my raw input:*
[Insert unstructured notes here]

Please organize this information into a structured interview summary using the following format:

---

## Overall Evaluation:

- **Appropriate for position?**: [Yes/No]  
- **Refer to Other Opportunities**: [Yes/No/Maybe, If Yes - Suggest roles or opportunities best suited to their strengths and areas for improvement.]  
- **Recommended Grade**: [Provide an overall grade, e.g., Junior, Middle, Senior]  

---

##General Impression:
[Summarize your overall impression of the candidate, including their demeanor, communication skills, and attitude during the interview. What is lack for next candidate grade. 1-2 paragraphs]  

## Key Strengths:
[Bullet list]

## Areas for Improvement:
[Bullet list]

---

## Assessment of Key Areas

1. **Programming Skills (Scala, Java, etc.)e**  
   [Summarize candidate’s proficiency in languages, focusing on core concepts, practical application, and knowledge depth. Provide examples if applicable.]  

2. **Big Data Technologies (Hadoop, Spark, Kafka, etc.)**  
   - **Hadoop (HDFS / Yarn / MapReduce / Hive / Pig / Parquet / Avro, etc.)**: [Summarize the candidate’s proficiency with Hadoop-related tools.]  
   - **Spark and Spark Streaming**: [Provide feedback on their experience and comfort level with Spark.]  
   - **Kafka / Beam / Flink / Ignite / NiFi / StreamSets, etc.**: [Evaluate their familiarity and expertise with other Big Data frameworks.]   

3. **Algorithms**  
   [Comment on the candidate’s algorithmic problem-solving skills, highlighting their approach, accuracy, and efficiency.]  


4. **SQL/NoSQL**  
   [Evaluate the candidate’s SQL skills, including their understanding of queries, optimization techniques, and handling complex data operations.]  

5. **Data Processing approaches (batch processing, stream processing)**  
   - **Batch Processing**: [Comment on their proficiency with batch processing approaches and technologies.]  
   - **Stream Processing**: [Evaluate their understanding and experience with stream processing technologies.]  

6. **Parallel Distributed Processing**

7. **Workflow Schedulers (Airflow, Oozie, Azkaban, Taverna, etc.)**


8. **Data Processing & Pipelines**  


9. **Cloud Services**  
   - **Google Cloud (GCP)**: [Assess their knowledge and experience with GCP tools and services.]  
   - **AWS**: [Summarize their understanding and practical application of AWS services.]  
   - **Azure**: [Provide feedback on their Azure-related experience.]  

---

## Coding Task Performance

- **Test Task #1: Algorithms**  
   [Provide a description of the task and evaluate the candidate’s performance, highlighting their approach and correctness.]  

- **Test Task #2: Spark**  
   [Provide a description of the Spark task and assess how effectively the candidate solved it.]  
