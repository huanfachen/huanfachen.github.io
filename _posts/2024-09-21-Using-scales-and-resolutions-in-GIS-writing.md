---
 layout: post


---

Updates 2024/09/21

This post discusses the issue of using *scales*, *resolution*, and *granularity* in the writing of GIS papers.

## Scales in GIS

Well, the topic of scale is a headache to most GIS people. In the GIS bible, the authors described "The Many Meanings of Scale", as below:

```
The concept of scale is fundamental to GIS, but unfortunately the word has acquired too many meanings in the course of time... it is best to use other terms that have clearer meaning where appropriate... In this book we have tried to avoid this problem [of many meanings of scale] by using the terms **coarse** and **fine** instead.
```

Long story short, there are at least three meanings of scale:

**Scale is in the details (for an average scientist)**. Many scientists (within and beyond GIS domain) use scale in the sense of spatial resolution, or the level of spatial detail in data. Data are fine-scaled or fine-grained (or at a fine level of granularity) if they include records of small objects, and coarse-scaled (or coarse-grained) if they do not.

**Scale is about extent (for an average scientist)**. People use scale to talk about the geographic extent or scope of a project: a large-scale project covers a large area. In addition, scale can also refer to other aspects of the project's scope, including the cost or the number of people involved.

**The scale of a map (for GIS scientists or cartographers)**. They use the term scale to refer to a map's *representative fraction*—the ratio of distance on the map to distance on the ground. Hence, a ‘large-scale map’ shows a relatively small area of the earth, such as a county or city, and a ‘small-scale map’ shows a relatively large area, such as a continent or a hemisphere of the earth.

## Spatial resolution

The term of spatial resolution comes from remote sensing. In remote sensing, three key aspects of resolution are spatial, spectral, and temporal. Spatial resolution refers to the size of object that can be resolved, and the most usual measure is the pixel size on the ground. For example, the spatial resolution of digital cameras used for capturing aerial photographs usually range from 0.01 m–5 m; this sensor is at a spatial resolution of 1.5 m.

Temporal resolution, or repeat cycle, describes the frequency with which images are collected for the same area.

## Examples of using scale/resolution in GIS papers

So, how should we use 'scale' (or 'resolution'), in combination with fine and coarse, to describe the spatial resolution/details of GIS research? Below are examples from this book

*P83*: it is not necessary to hide any data in the choropleth map shown in Figure 4.7B because privacy is not violated at this **coarser level of granularity**. 

*P123*: This gives rise to the related aggregation or zonation problem, in which different combinations of a given number of geographic individuals into **coarser-scale areal units** can yield widely different results.

*P178*: the spatial resolution of commercial satellites is **too coarse** for many detailed projects, and the data collection capability of many sensors is restricted by cloud cover.

*P340*: Spatial and temporal resolution also determine the cost of acquiring the data because in general it is more costly to collect a fine-resolution representation than a **coarse-resolution** one.

### Examples describing the spatial resolution of a study

People rarely say 'The spatial resolution of this analysis is a 100-meter by 100-meter grid'. 

Instead, the three following statements are used:

1. The spatial resolution of this analysis is 100 meters.
2. The spatial resolution of the analysis presented in this paper corresponds to a 100-meter by 100-meter grid.
3. This paper presents an analysis at a spatial resolution of 100 meters by 100 meters

Other examples:

*P62*: Figure 3.4 shows Manhattan at a spatial resolution of 250 m, detailed enough to pick out the shape of the island and Central Park

*P223*: Does it have sufficient spatial resolution and acceptable quality? 

(From another paper): Flow data are aggregated in a **high-resolution grid** with temporal and spatial granularity of 10 minutes and 500 m, respectively. (high-resolution means fine-resolution)

## Granularity

In GIS domain, granularity seems very similar to resolution. Usually, granularity is used along with fine or coarse.

*P401*: The global coverage, quality, and currency of some crucial datasets—especially those pertaining to human beings at fine spatial granularity—are highly variable.

*P56*: The spatial and temporal granularity of the diagram is set in such a way that even quite small events are recorded

## Geographic unit

In Section 5.2, the authors used the term 'geographic unit of analysis' to describe the spatial unit in the analysis when discussing uncertainty in the conception of geographic phenomena.

In writing a GIS paper, how should we describe the geographic unit of analysis?

(Weisburd et al 2009) In the 19th century, they typically studied large administrative districts such as regions and countries. The Chicago School focused on much smaller urban communities. More recently, interest has moved toward *geographic units* as small as street blocks or addresses. After this historical account, we address specific questions regarding how the unit of analysis should be chosen for crime and place studies.

For example, how should we describe that we use MSOA (Middle-layer Super Output Area) as the geographic unit in the analysis?
