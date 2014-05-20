code for Large Scale Hierarchical Text Classification competition.

http://www.kaggle.com/c/lshtc

# Summary

a centroid-based flat classifier.

1. Extract K-candidate categories by Nearest Centroid Classifier.
2. Remove some missclassified categories by Binary Classifier from candidate categories.

# Requirements

- Ubuntu 13.10
- g++ 4.8.1
- make
- 32GB RAM

# How to Generate the Solution

please edit SETTINGS.h first.

    make
    ./prefetch
    ./train
    ./predict

NOTE: ./prefetch is very slow. probably processing time exceeds 15 hours.

# MISC programs

## Running the Validation Test

    ./vt_prefech
    ./vt_train
    ./validation

## Simple k-NN baseline

validation test.

    ./vt_knn

generate sumission.txt.

    ./knn

## Simple Nearest Centroid Classifier

validation test.

    ./vt_ncc

generate sumission.txt.

    ./ncc

## Figure

<table>
  <tr>
     <th>Model</th><th>LBMaF</th><th>Training Time</th><th>Prediction Time</th>
  </tr>
  <tr>
    <td>k-NN</td><td>0.23088</td><td>n/a</td><td>10 minutes</td>
  </tr>
  <tr>
    <td>NCC</td><td>0.28931</td><td>80 seconds</td><td>2 hours</td>
  </tr>
  <tr>
    <td>NCC+BC</td><td>0.33025</td><td>15 hours</td><td>2 hours</td>
  </tr>
</table>
