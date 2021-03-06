# Limitations

While very powerful and flexible, TRACER also has limitations.

## Garbage in, garbage out

The quality and accuracy of the results computer by TRACER depend on the quality of input data. If the corpus is dirty or if the linguistic resources \(lemma files, WordNets, etc.\) are suboptimal, the results of TRACER will be affected. So, the higher the quality of the input data, the better the TRACER results.

## Visualisation of text reuse results

Another limitation of TRACER concerns the visualisation of the computed text reuse results. While adequate to display small data, TRAViz is not well-suited for visualising a large number of results \(e.g. comparing 10 texts against one another\). This is because the underlying code of TRAViz \(JavaScript\) is not able to process and load large amounts of information.

## Absence of _code_ documentation

The ca. 700 algorithms constituting TRACER are accessible through TRACER's Javadoc but are not documented in detail. This is an issue for those wishing to reuse TRACER's code in other projects but to provide a short description for every algorithm in TRACER would require significant resources. This user manual serves as a compromise and describes the most popular algorithms for this type of textual analysis.

