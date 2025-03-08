# Temporal Scene-Text Calibrating and Distilling for Text-Video Retrieval


## [1/7] Task Introduction 

<div style="display: flex; justify-content: space-between;">
    <figure>
        <img src="images/task.png" alt="Introduction Image" style="width: 100%;">
    </figure>
</div>

<p align="justify">
<b>Figure 1:</b> (a) Existing methods overlook the fine-grained scene
text in videos. (b) SOTA method [53] handles scene text as an in-
stance, resulting in token imbalance issue that hinders fine-grained
interaction. (d) Our window-OCR captioner aggregates abundant
scene text into condensed sentences for fine-grained interaction,
achieving better performance with lower complexity (c).
</p>

## [2/7] Model Architecture
![TCD Model Architecture](images/T-CARD.png)

<p align="justify">
<b>Figure 2:</b> Pipeline of the proposed <b>TCD</b>. Window-OCR captioner is leveraged to aggregate abundant scene text into condensed OCR captions. Heterogeneous semantics calibrating uses scene text in both video frames and OCR captions as a signal for self-supervised learning. Context-guided temporal clue distilling assigns each modal query with a learnable clue to obtain a clear context temporal clue.
</p>



<!-- <div style="display: flex; justify-content: space-between;">
    <figure>
        <video controls style="width: 100%;">
            <source src="video.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </figure>
</div> -->

## [3/7] Window-OCR Captioner 🌟🌟🌟

<div style="display: flex; justify-content: space-between;">
    <figure>
        <img src="images/Visualization_demo.gif" alt="New Visualization" style="width: 100%;">
    </figure>
</div>

<p align="justify">
<b>Figure 3:</b> Visualization of the proposed Window-OCR Captioner. We aggregrate different kinds of scene texts appearing within a window length of ∆t into a single caption to reduce the feature length from N in previous works (e.g., StarVR [53]) to 1.
</p>

## [4/7] Heterogeneous Semantics Calibrating

<div style="display: flex; justify-content: space-between;">
    <figure>
        <img src="images/HSC_demo.gif" alt="HSC demo" style="width: 100%;">
    </figure>
</div>

<!-- <div style="display: flex; justify-content: space-between;">
    <figure>
        <video controls style="width: 100%;">
            <source src="video2.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </figure>
</div> -->


## [5/7] Text→Video Retrieval Results (1/2)
![Text→Video Retrieval (1/2)](images/t2v_2.png)
<p align="justify">
<b>Figure 4:</b> Visualization of retrieval results comparing our method (left) with the model without OCR information (right). Sim indicates the overall similarity
score, calculated as the average of text-OCR, text-video, and text-hybrid matching scores, denoted as OCR, Video, and Hybrid, respectively. Our TCD captures fine-grained scene text, such as "GRILL" and "Thank you" with high similarity and hybrid scores. Please zoom in for a better view of the details.
</p>

## [6/7] Text→Video Retrieval Results (2/2)
![Text→Video Retrieval (2/2)](images/t2v_1.png)
<p align="justify">
<b>Figure 5:</b> Visualization of retrieval results comparing our method (left) with the model without OCR information (right). Sim represents the overall similarity
score, calculated as the average of text-OCR, text-video, and text-hybrid matching scores, denoted as OCR, Video, and Hybrid, respectively. Our TCD captures fine-grained scene text, such as "SAC MIA", "School", and "SDY 288H" with high similarity and hybrid scores. Please zoom in for a better view of the details.
</p>




## [7/7] Abstract
<div style="text-align: justify;">
Existing text-video retrieval (TVR) methods mainly focus on aligning single-modal video content with text queries, overlooking heterogeneous scene text in videos. While scene text offers fine-grained semantics for cross-modal matching, its effective utilization faces two critical challenges: (1) The temporal density of scene text imposes substantial computational burdens, and (2) Redundant scene text and irrelevant video frames hinder the learning of clear temporal clues for retrieval. In this paper, we propose a temporal scene-text calibrating and distilling (TCD) network to encode scene text efficiently while capturing clear temporal clues. Concretely, we first design a window-OCR captioner that aggregates abundant scene text in videos into condensed sentences to reduce computational complexity. Then, we leverage the heterogeneous scene text as a self-supervised signal to calibrate the synchronization between window-level OCR captions and frames-level video sequences. Furthermore, we devise a context-guided temporal clue distillation to capture the complementarity and relevance among scene text and video frames, generating clear temporal clues for retrieval. Extensive experiments show TCD achieves SOTA results on two scene text TVR datasets and one traditional TVR dataset.
</div>

**The source code and trained models will be released soon.**
