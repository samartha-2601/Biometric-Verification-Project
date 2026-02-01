# Offline Biometric Verification and Authentication

A deep learning system for user authentication using signature and fingerprint verification with Siamese Neural Networks and ORB matching.

## Overview

Automated biometric verification system that replaces manual signature and fingerprint inspection. Uses Siamese CNNs for signature verification and ORB similarity for fingerprint matching.

## Features

- **Dual Authentication**: Signature + fingerprint verification
- **Offline Processing**: Works with scanned images, no specialized hardware needed
- **One-Shot Learning**: Minimal training data required per user
- **Web Interface**: Flask-based signup, login, and transaction verification
- **High Accuracy**: >85% with low false positive rate

## Tech Stack

- **Backend**: Python, Flask, TensorFlow
- **Database**: MongoDB
- **Computer Vision**: OpenCV
- **Algorithms**: Siamese Neural Networks, ORB Feature Matching

## Datasets

- **CEDAR**: 1,320 genuine + 1,320 forged signatures (55 users)
- **SOCOFing**: 6,000 fingerprint images (600 subjects)

## System Architecture
```
User Input → Flask Server → ML Models → MongoDB → Response
                             ↓
                    Signature (Siamese CNN)
                    Fingerprint (ORB Matching)
```

## Algorithms

### Siamese Network (Signature)
- Twin CNNs with shared weights
- Learns similarity metric using triplet loss
- Compares input signature with stored template

### ORB Matching (Fingerprint)
- FAST keypoint detection + BRIEF descriptors
- Brute force matching with threshold filtering
- Fast and efficient matching

## Results

- **Peak Accuracy**: ~95% (signature verification)
- **F1 Score**: ~0.95 at optimal threshold
- **Response Time**: Minimal latency for real-time use


## Team

**Students**: Niranjan Hegde (1BM19IS103), Samartha S (1BM19IS219)

**Supervisor**: Mrs. Nalina V, Assistant Professor

**Institution**: B.M.S. College of Engineering, Dept. of ISE


---

**Note**: Academic project developed at B.M.S. College of Engineering for educational purposes.
