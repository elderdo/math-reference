# The Mathematics of Paper & Rectangle Folding

A comprehensive guide to the geometric algorithms and combinatorics underlying the complex folding challenges popularized by recreational mathematicians like Matt Parker.

---

## 1. The Fold-and-Cut Theorem (Straight-Line Cuts)
The Fold-and-Cut Theorem proves that any geometric shape or polygon with straight edges can be completely cut out of a rectangular sheet of paper with a **single straight snip** of scissors, provided the paper is pre-folded along a specific set of creases.

### Core Mathematical Concepts
* **Straight-Line Skeletons:** This algorithm uses internal bisectors and geometric paths to align all the edges of a target shape perfectly along a single straight line before the cut is made.
* **Flat-Foldability:** The study of the mathematical conditions (such as Kawasaki's Theorem and Maekawa's Theorem) required for a 3D crease pattern to fold down completely into a flat 2D plane.

### Video Tutorials & Slide Resources

* **MIT 6.849: Geometric Folding Algorithms**
  * *Instructor:* Professor Erik Demaine
  * *Overview:* The gold-standard graduate-level university course covering origami, linkages, and polyhedra. Lectures 17 and 18 explicitly deep-dive into the Fold-and-Cut Theorem and straight-line skeletons.
  * *Video Lectures:* Available for free on the [MIT OpenCourseWare YouTube Channel](https://www.youtube.com/@mitocw).
  * *Slide/PowerPoint Downloads:* Download full lecture slides, geometric problem sets, and syllabi directly from the official [MIT OCW Course Page](https://ocw.mit.edu/courses/6-849-geometric-folding-algorithms-linkages-origami-polyhedra-fall-2012/) or [ErikDemaine.org](https://erikdemaine.org/classes/).

* **Numberphile: "Fold and Cut Theorem"**
  * *Featuring:* Dr. Katie Steckles
  * *Overview:* A highly visual, accessible, and physical demonstration of the geometric properties of folding letters of the alphabet into single-cut layouts.
  * *Video Lecture:* Available on the [Numberphile YouTube Channel](https://www.youtube.com/@Numberphile).

---

## 2. The Stack-Folding & Map-Folding Problem
Stack-folding puzzles (such as folding an $n \times n$ or linear grid of lettered rectangles into a sequential stack) belong to classic combinatorics problems known as the **Stamp Folding** and **Map Folding** problems.

### Core Mathematical Concepts
* **Permutations & Topology:** Folding a grid introduces physical constraints where adjacent sections create boundaries. Folds cannot intersect, cross, or tear the continuous paper medium.
* **Face Orientation Parity:** Tracking whether a section lands face-up or face-down is governed by strict binary alternating parity. This is based on the number and direction of the orthogonal folds executed across the grid.

### Video Tutorials & Resources

* **"How Many Ways Can You Fold a Map?"**
  * *Overview:* A dedicated math exploration breaking down the exact formulas, permutations, and leaf-order rules governing a grid of rectangles. It details why counting map folds scales exponentially into a notoriously difficult unsolved problem.
  * *Video Link:* Search for "How Many Ways Can You Fold a Map?" on YouTube.

* **MIT 6.006: Introduction to Algorithms**
  * *Overview:* Provides broader algorithmic context on how computational geometry handles folding patterns, matrix algebra transformations, and flat-foldability constraints.
  * *Video Lecture:* See [Lecture 21: Algorithms—Next Steps](https://www.youtube.com/watch?v=R9KREwV9I_U) on the MIT OpenCourseWare YouTube channel.

---

## How to Utilize the Material Effectively
1. **Download Blueprints:** Go to the [MIT OCW 6.849 Course Page](https://ocw.mit.edu/courses/6-849-geometric-folding-algorithms-linkages-origami-polyhedra-fall-2012/).
2. **Access Lecture Notes:** Navigate to the **"Lecture Notes"** or **"Assignments"** tab to download PDFs and slides explaining **Voronoi diagrams** and **straight skeletons**.
3. **Analyze Crease Patterns:** Use these files to see why paper must be folded along specific bisecting angles to achieve desired shapes.
