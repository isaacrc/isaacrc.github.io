---
layout: archive
title: "Open reviews"
permalink: /reviews/2023-04-24-vigliocco
author_profile: true
---

{% include base_path %}


### April 24, 2023 &mdash; Open review of preprint by Vigliocco and colleagues:
Vigliocco, G., Conventino, L., De Felice, S., Gregorians, L., Kewenig, V., Mueller, M. A., Veselic, S., Musolesi, M., Hudson-Smith, A., Tyler, N., Flouri, E., & Spiers, H. (2023). Ecological brain: reframing the study of human behaviour and cognition. *PsyArXiv*. [`DOI`](https://doi.org/10.31234/osf.io/zr4nm)

---

Vigliocco and colleagues outline their vision for a more “ecological” science of brain and behavior. They propose a cyclic interplay between exploratory real-world research and more targeted, confirmatory laboratory research: data-driven, observational research in the real world generates hypotheses for more ecologically generalizable laboratory research, and laboratory manipulations in turn are extended to and evaluated in real-world contexts. They emphasize the importance of interdisciplinary expertise for this approach, and outline a variety of new tools and technologies for studying brain and behavior with greater ecological validity. The article is well-written, well-referenced, and I find myself agreeing with most of the authors’ sentiments. My overall feeling is that the authors could go even further. In some ways the manuscript feels cautious. I’m already embedded in this kind of research, so I’m obviously biased and may not be a representative reader—but I worry that a reader will think “I agree, and we’re *already* trying to do all of this!” It’s tricky to review perspective pieces like this, but I’ll outline some thoughts below—take everything with a grain of salt!

### Major comments:

Here’s the main thing that I felt was “missing” from this piece: The authors focus on the paradigm shift toward more ecological data, but in my mind, the most important advance for naturalistic neuroscience and psychology in the last decade has been the development of computational models that can actually cope with messy, real-world data—models that respect the richness of context and can actually reproduce complex human behaviors (e.g. image/face recognition, language production). I see several “keys” to developing models like this: (1) relaxing our demands that the model be low-dimensional and easily interpretable; instead we use a high-dimensional, expressive learning model; (2) evaluate the model in terms of how well it can actually perform the real-world task (i.e. using out-of-sample prediction), rather than in terms of interpretability or how well the model fits particular experimental data; (3) instead of “engineering” small, tightly controlled datasets to inform our models, we feed the model all of the noisy, real-world data we can find and see what structure emerges from the learning process. This is in stark contrast to the kind of modeling traditionally used in psychology and neuroscience: historically, we develop concise, interpretable models of tightly controlled experimental phenomena. That is, we start with a simple, interpretable model of some very particular aspect of the object of study, and use experimental manipulations to generate data that can inform that model. Suddenly, we have models that can actually perform holistic behaviors (e.g. read a block of text and effectively summarize it; comprehend questions and provide reasonable answers); this opens all sorts of new doors. This paradigm shift toward real-world models has several ramifications related to topics discussed in the current work that could be worth discussing; I try to outline these ramifications in the next three comments.

Related to the previous point, real-world research doesn’t need to be strictly exploratory; we can still “test hypotheses” (in a fashion) against naturalistic data. Here I’m invoking the “system identification” approach popularized by Gallant and colleagues (e.g. [Wu et al., 2006](https://doi.org/10.1146/annurev.neuro.29.051605.113024)): instead of manufacturing laboratory data to test a particular hypothesis, we formulate our hypotheses as explicit models and evaluate these models according to their out-of-sample prediction in real-world data. To test a very targeted hypothesis, we develop a model that incorporates that hypothesis and compare that model’s performance to the most similar possible model that doesn’t include the hypothesized component. To pit hypotheses against each other, we develop models that embody the respective hypotheses and compare their prediction performances. This approach forces us to at least formulate our hypotheses in a way that can accommodate real-world data.

I didn’t find the authors’ treatment of “context” (page 8) very compelling. I agree that “context” is often used imprecisely, but I think context is much more fundamental to cognition than just “everything that is not manipulated or measured.” I don’t think it’s an exaggeration to say that all cognition happens in context; and I would venture that the vast majority of cognition is context-sensitive. To me, Gomez-Marin and Ghazanfar ([2019](https://doi.org/10.1016/j.neuron.2019.09.017)) provide the most compelling treatment of this topic. I also don’t know if it will ever be realistic or feasible for all contextual factors to be “specified, characterised and included among the experimental variables.” However, if our goal is to “generalise to the ‘real world’” or to discover invariances in brain activity and behavior across contexts, the previously mentioned modeling framework provides a straightforward way to do so: out-of-sample prediction. When we move to a modeling framework using out-of-sample prediction (the standard in machine learning), the assessment of generalization is straightforward and baked in. If you want to evaluate whether your model of a particular phenomenon generalizes across contexts, build or train your model in one (subset of) context(s) and evaluate its prediction performance in a novel context.

My reading of the section “Theories must incorporate the environment” leans more toward “theories must incorporate *context*”—but I worry that the kinds of theories many of us seek for brain and behavior won’t *ever* be able to account for the richness and variety of context, because they hedge too closely to low-dimensional, human-interpretable model features. Put differently, sociobiological phenomena like human brain activity and behavior may simply not be amenable to the style of theories we’ve imported from the natural sciences. What if an important “universal” principle is “context-sensitivity”? My worry stems from the observation that (in my understanding) the only models we’ve discovered so far that actually get even close to respecting the contextual richness of real-world vision or real-world language are high-dimensional learning models (i.e. deep neural networks, transformers) that can absorb the rich structure of real-world contexts without the fetters of low-dimensionality / ease-of-interpretation.

Another important feature of real-world research that seems underemphasized here is that it allows scientists to evaluate the relative contributions of different constructs or models when combined in real-world contexts. Most laboratory research uses experimental manipulations to target or isolate particular variables to model; but these different variables/models are rarely recombined in real-world contexts to evaluate their relative contributions and interactions (in my experience, it’s often difficult to even imagine how these variables/models would be combined into a joint model). This seems like it should be an important consideration when planning future research so that we don’t dedicate years of work to phenomena that account for a negligible proportion of variance in real-world behavior and brain activity. Obviously phenomena that account for very little variance in real-world contexts can still reveal important findings (e.g. “controversial” experiments that use edge cases to adjudicate between models; [Golan et al., 2020](https://doi.org/10.1073/pnas.1912334117)), but these findings should be interpreted in light of their relative importance under ecological circumstances.

One thing that might be interesting to discuss in brief is the demands this approach can put on trainees. In my experience, the default training model for PhD students (and some postdocs) follows the classical “bench scientist” model, where a student is expected to show up, design a laboratory experiment to test a particular hypothesis, collect a manageable dataset to test this hypothesis, analyze their data and run the statistical test, then write up the paper. In my experience, naturalistic research doesn’t usually unfold this way. The datasets are often bigger, messier, and require considerably more expertise in skills like data wrangling, engineering, or machine learning. This may result in a more protracted, team-based research approach, where different people serve as domain experts in different parts of the research process, rather than a single researcher taking everything from start to finish. But, if these scientists are then evaluated individually in terms of their “ownership” over an entire project, we might run into problems. Do the authors have any thoughts on how our pedagogy or incentive structures should change to better support this kind of research?

### Minor comments:

I didn’t find the section on replicability to be very convincing. The problem of replicability stems from a variety of issues (small samples, p-hacking) that don’t directly relate to ecological validity. Some aspects of non-replicability may be ameliorated by improved ecological validity; but many of the proposed improvements to replicability (e.g. increased sample sizes) will have little to no impact on ecological generalizability. We can take steps to ensure that a particular laboratory manipulation is highly replicable, but that doesn’t mean it has any relevance to real-world behavior.

Page 4, line 25: “human behaviour, real-world environments” —this seems to leave out the brain, which is important because the theories and tools needed to understand the brain may be different from those needed to understand behavior.

Page 7, line 24: “solves key problems with reductionism” > “solves key problems of reductionism” to rule out the gloss that the ecological brain framework is *using reductionism* to solve key problems.

On page 9, you pose the question of “why practices have not yet fully changed”—I agree that the transition is challenging and the incentives are ill-fitting, but I would also contend that oftentimes we’re wedded to a style of theories/models that will *never* support ecological generalizability for the kinds of phenomena we study (as I outlined in my previous comments).

The paper is already very well-referenced, but there are a couple papers that occurred to me while reading as potentially relevant (the authors can choose to include/exclude at their discretion): (1) When you talk about reductionism and discuss the assumption that “mental events must be parcellated in order to be scientifically tractable,” work by Paul Cisek seems very relevant (e.g. [Cisek & Kalaska, 2010](https://doi.org/10.1146/annurev.neuro.051508.135409); [Cisek, 2019](https://doi.org/10.3758/s13414-019-01760-1)); (2) When you talk about how “exploratory research is necessary to identify key variables,” this made me think of a paper by Paul Rozin ([2001](https://doi.org/10.1207/S15327957PSPR0501_1)) about how (social) psychology may have prematurely committed to a particular kind of science (controlled laboratory experiments) and could benefit from taking a step back and deploying a wider variety of methods (e.g. observational research); (3) Tal Yarkoni’s recent ([2022](https://doi.org/10.1017/S0140525X20001685)) paper also seems broadly relevant to the limited generalizability of the dominant statistical framework.

### References:

Cisek, P., & Kalaska, J. F. (2010). Neural mechanisms for interacting with a world full of action choices. *Annual Review of Neuroscience*, *33*, 269–298. [`DOI`](https://doi.org/10.1146/annurev.neuro.051508.135409)

Cisek, P. (2019). Resynthesizing behavior through phylogenetic refinement. *Attention, Perception, & Psychophysics*, *81*, 2265–2287. [`DOI`](https://doi.org/10.3758/s13414-019-01760-1)

Golan, T., Raju, P. C., & Kriegeskorte, N. (2020). Controversial stimuli: pitting neural networks against each other as models of human cognition. *Proceedings of the National Academy of Sciences*, *117*(47), 29330–29337. [`DOI`](https://doi.org/10.1073/pnas.1912334117)

Gomez-Marin, A., & Ghazanfar, A. A. (2019). The life of behavior. *Neuron*, *104*(1), 25-36. [`DOI`](https://doi.org/10.1016/j.neuron.2019.09.017)

Rozin, P. (2001). Social psychology and science: some lessons from Solomon Asch. *Personality and Social Psychology Review*, *5*(1), 2–14. [`DOI`](https://doi.org/10.1207/S15327957PSPR0501_1)

Yarkoni, T. (2022). The generalizability crisis. *Behavioral and Brain Sciences*, *45*, e1. [`DOI`](https://doi.org/10.1017/S0140525X20001685)

Wu, M. C. K., David, S. V., & Gallant, J. L. (2006). Complete functional characterization of sensory neurons by system identification. *Annual Review of Neuroscience*, *29*, 477-505. [`DOI`](https://doi.org/10.1146/annurev.neuro.29.051605.113024)
