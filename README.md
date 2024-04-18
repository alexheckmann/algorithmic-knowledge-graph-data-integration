# Algorithmic Knowledge Graph Data Integration

Knowledge Graphs (KGs) are a powerful tool for representing and querying structured information. However, creating and
maintaining a KG is a complex and time-consuming task. In this project, we propose an algorithmic approach to
automatically
generate a KG from a set of structured data sources. Our approach leverages the power of KG embeddings to learn a
unified representation of the data sources and then uses this representation to generate a KG. We evaluate our approach
on a real-world dataset and show that it can effectively generate a KG that captures the relationships between the data
sources.

The dataset is based on restaurants in the US and their menus. The goal is to insert the data into the knowledge graph
so that this flat tabular data gets transformed into semantically rich data that can be used for e.g. LLM-based
recommendation systems.

## The algorithm

The approach taken in this project was mostly programmatic using Python and RDFlib.

It was mostly based on regular expressions, string manipulation, and data transformation.

Machine learning-based approaches
were out of scope for this project due to time constraints. Nonetheless, the project was successful in transforming the
tabular data into a knowledge graph with only a information loss 2.67% and a good performance in terms of
algorithmic time and space complexity.

## Testing

The project was tested using a set of SparQL queries that were run against the generated knowledge graph. The queries
were designed to test the correctness of the transformation and the completeness of the data.
They were presented in increasing complexity and were run against the knowledge graph to check if the expected results
were returned.

## Alignment

The project also included an alignment step where the generated knowledge graph was aligned with an existing ontology.
This step was crucial to ensure that the generated knowledge graph was semantically rich and could be used in
applications that require a high level of semantic understanding.

The comparison was done using the SequenceMatcher class from the difflib module in Python, i.e. a simple common
subsequence algorithm. Once again, due to time constraints, a more sophisticated algorithm was not implemented.

The alignment was successful, and the generated knowledge graph was aligned with the existing ontology with a high
degree of accuracy, with only 3 triples being mismatched.

