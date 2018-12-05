# Figures

Hopefully Github will enable [rendering of graphs](https://github.com/github/markup/issues/533) one day... The figure below is a screenshot from the rendering in [Typora](https://typora.io).

## special_values figure

This is the code for the  [mermaid graph](https://mermaidjs.github.io) in the [codebook.md](../../codebook.md) file. 



```mermaid
graph TD

%% Items
NULL["#quot;NULL#quot;<br/>(no observation)"]
has_info[<i>Does the data source<br/>contain any information?</i>]
NA["#quot;NA#quot;</br>(no information)"]
is_numerical["<i>Does the data source contain<br/>numerical information?</i>"]
unspecified["#quot;unspecified#quot;"]
is_zero["<i>Does the data source</br>specify the value 0?</i>"]
number["#quot;number#quot;"]
zero["#quot;0#quot;"]

%% Connectors
NULL-->has_info;
has_info--"No"-->NA;
has_info--"Yes"-->is_numerical;
is_numerical--"No"-->unspecified;
is_numerical--"Yes"-->is_zero;
is_zero--"No"-->number;
is_zero--"Yes"-->zero;

%% Style – https://websafecolors.info/color-chart
%% e.g. style id2 fill:#ccf,stroke:#f66,stroke-width:2px,stroke-dasharray: 5, 5

%% linkStyle 1 fill:transparent;
style NULL fill:transparent,stroke:transparent;
style has_info fill:transparent,stroke:transparent;
style NA fill:transparent,stroke:transparent;
style is_numerical fill:transparent,stroke:transparent;
style unspecified fill:transparent,stroke:transparent;
style is_zero fill:transparent,stroke:transparent;
style number fill:transparent,stroke:transparent;
style zero fill:transparent,stroke:transparent;
style has_info fill:transparent,stroke:transparent;
```
















