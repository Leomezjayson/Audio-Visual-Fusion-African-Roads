# Contributing to SenseAI Research

> *"Standing on the shoulders of giants to build for Africa."*

Thank you for your interest in contributing to the SenseAI Research project! This is an open-source research project with a commercial roadmap. Your contributions—whether code, bug reports, or research insights—are invaluable.

Before contributing, please take a moment to read this document. It will save time and ensure your contributions are accepted smoothly.

---

## 📌 Table of Contents

1. [Code of Conduct](#-code-of-conduct)
2. [What We Need Help With](#-what-we-need-help-with)
3. [Getting Started](#-getting-started)
4. [How to Contribute](#-how-to-contribute)
5. [Contribution Guidelines](#-contribution-guidelines)
6. [Style Guide](#-style-guide)
7. [Testing Requirements](#-testing-requirements)
8. [Documentation](#-documentation)
9. [Intellectual Property & Licensing](#-intellectual-property--licensing)
10. [Review Process](#-review-process)
11. [Getting Help](#-getting-help)

---
## 🤝 Code of Conduct

We are committed to fostering an open, welcoming, and inclusive environment. By participating in this project, you agree to abide by our [Code of Conduct](CODE_OF_CONDUCT.md).

**In short:**
- Be respectful and kind
- Provide constructive feedback
- Assume good intentions
- Avoid harassment, discrimination, or offensive behavior

---

## 🎯 What We Need Help With

We welcome contributions in the following areas:

### 🧠 Research & Data
- **Dataset Collection:** Record driving footage in African cities (we provide guidelines)
- **Data Annotation:** Label videos and audio using CVAT or similar tools
- **Literature Review:** Summarize recent papers on audio-visual fusion
- **Benchmarking:** Test our models against new datasets

### 💻 Code
- **Vision Encoders:** Improve ResNet50 or add newer architectures (ViT, DINOv2)
- **Audio Encoders:** Experiment with newer audio transformers
- **Fusion Mechanisms:** Propose and implement novel fusion strategies
- **Edge Optimization:** Port models to TensorFlow Lite, ONNX, or WebRTC

### 📚 Documentation
- **Tutorials:** Write notebooks explaining how to use the code
- **API Documentation:** Improve docstrings and comments
- **Translations:** Translate documentation into local African languages

### 🌍 Community & Outreach
- **Blog Posts:** Write about your experiments and learnings
- **Social Media:** Share your experiences using the project
- **Workshops:** Host tutorials at your university or meetup

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10+
- Git
- PyTorch or TensorFlow (check `requirements.txt`)
- Basic understanding of computer vision and/or audio processing


### Setup

```bash
# Fork the repository (click the "Fork" button on GitHub)
git clone https://github.com/Leomezjayson/senseai-research.git
cd senseai-research

# Add upstream remote
git remote add upstream https://github.com/original-owner/senseai-research.git

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Install pre-commit hooks (optional but recommended)
pre-commit install
First Contribution: Find a Good First Issue

Check the Issues page and look for labels:

· good first issue
· help wanted
· research
· documentation

---
```
📝 How to Contribute

1. Fork & Clone

1. Fork the repository on GitHub
2. Clone your fork locally
3. Add the upstream remote

2. Create a Branch

Use a descriptive branch name:

· feature/add-new-encoder
· bug/fix-data-loading
· research/experiment-fusion-strategy
· docs/update-readme

```bash
git checkout -b feature/your-feature-name
```

3. Make Your Changes

· Write clean, readable, and commented code
· Add tests for new functionality
· Update documentation where relevant

4. Test Your Changes

```bash
# Run all tests
pytest tests/

# Run linting and formatting checks
black src/ notebooks/
flake8 src/
isort .
```

5. Commit & Push

Write meaningful commit messages:

```bash
git add .
git commit -m "feat: add new vision encoder for low-light conditions"
git push origin feature/your-feature-name
```

6. Submit a Pull Request

· Go to the original repository
· Click "New Pull Request"
· Select your branch and describe your changes
· Reference any relevant issues

---

📋 Contribution Guidelines

What We Accept

✅ New model architectures or encoders
· ✅ Performance improvements and optimizations
· ✅ Bug fixes and security patches
· ✅ Documentation improvements
· ✅ New datasets or data pipelines
· ✅ Reproducibility improvements
· ✅ Research insights and benchmarks

What We Do Not Accept

· ❌ Code that breaks existing functionality
· ❌ Contributions that violate intellectual property rights
· ❌ Unethical or harmful research applications
· ❌ Commercial code without proper licensing
· ❌ Plagiarized or uncredited work

---

🎨 Style Guide

Python

We follow PEP 8 guidelines. Use:

· Black for automatic formatting
· isort for import sorting
· flake8 for linting

Example:

```python
# Good
def calculate_fusion_weights(vision_confidence: float, audio_confidence: float) -> float:
    """Calculate dynamic fusion weight based on confidence scores.

    Args:
        vision_confidence (float): Vision branch confidence (0-1)
        audio_confidence (float): Audio branch confidence (0-1)

    Returns:
        float: Fusion weight alpha (0-1) where alpha = vision weight
    """
    # Dynamic weighting logic
    base_weight = 0.6  # Default vision dominance
    if vision_confidence < 0.3:
        return 0.3  # Audio dominance in low-vision scenarios
    return base_weight
```

Notebooks

· Use clear titles and headings
· Include markdown cells explaining your thought process
· Keep cells focused and well-commented
· Avoid long-running cells without progress indicators

Documentation

· Write in clear, simple English
· Use present tense
· Include code examples where helpful
· Add "See Also" sections for related work

---

🧪 Testing Requirements

All new code must include tests:

Unit Tests

```python
# tests/test_fusion.py
import pytest
from src.fusion import dynamic_fusion

def test_dynamic_fusion_low_vision():
    """Test fusion weight when vision confidence is low."""
    alpha = dynamic_fusion(vision_conf=0.2, audio_conf=0.9)
    assert alpha < 0.4  # Audio should dominate
```

Running Tests

```bash
# Run all tests
pytest tests/

# Run specific test file
pytest tests/test_fusion.py

# Run with coverage
pytest --cov=src tests/
```

Coverage requirement: >= 80% for new code

---

📚 Documentation

Docstrings

Use Google-style docstrings:

```python
def load_data(filepath: str, sample_rate: int = 16000) -> Dict[str, np.ndarray]:
    """Load audio and video data from file.

    Args:
        filepath (str): Path to the data file.
        sample_rate (int, optional): Audio sample rate. Defaults to 16000.

    Returns:
        Dict[str, np.ndarray]: Dictionary containing 'audio' and 'video' arrays.

    Raises:
        FileNotFoundError: If file does not exist.
    """
```

README Updates

If you add a major feature, update the README.md:

· Add a section explaining the new feature
· Include an example of how to use it
· Update the table of contents

---

⚖️ Intellectual Property & Licensing

By contributing, you agree that:

1. Your contributions will be licensed under the MIT License (for open-source components).
2. You have the right to submit the contribution.
3. You assign copyright of your contributions to the project author for licensing purposes.
4. You will not contribute proprietary code, data, or trade secrets.

For proprietary contributions (model weights, datasets):

· Contact the author directly at 1703240434@live.gctu.edu.gh
· We may negotiate separate commercial terms

---

🔍 Review Process

All pull requests go through the following stages:

1. Automated Checks (GitHub Actions)
   · Linting (flake8)
   · Formatting (Black)
   · Tests (pytest)
   · Code coverage check
2. Human Review
   · Code quality and readability
   · Documentation completeness
   · Test coverage
   · Alignment with project goals
3. Clarification & Revisions
   · Reviewers may request changes
   · You can push updates to your branch
   · The PR will be automatically updated
4. Merge
   · Maintainers merge approved PRs
   · Squash merging is preferred for clean history

Review Timeline

· Initial response: Within 3 business days
· Full review: Within 7 business days
· Complex PRs: Up to 14 business days

---

🆘 Getting Help

Channels

Channel Purpose
GitHub Issues: Bug reports, feature requests, questions
Discussions: Open-ended questions, ideas, community chat
Email: 1703240434@live.gctu.edu.gh Private/inquiries (commercial, research collaboration)

What to Include When Asking for Help

· Clear description of the problem
· Steps to reproduce (if bug)
· Relevant error messages
· Your environment (OS, Python version, package versions)
· What you've already tried

---

🏆 Acknowledgments

Contributors who make significant contributions may be:

· Listed in the CONTRIBUTORS.md file
· Added as repository collaborators
· Included in the thesis acknowledgments
· Offered co-authorship on publications (if contribution is substantial)

To be considered for co-authorship:

· Major algorithm design
· Novel dataset creation (100+ hours)
· Significant code refactoring
· Breakthrough experimental results

---

🌍 A Note on African Context

We prioritize contributions that:

· Address African road conditions (unstructured, high-density)
· Work with limited compute resources
· Are accessible to African researchers and developers
· Solve practical, locally relevant problems

Contributions from African researchers, students, and practitioners are especially welcome. Our goal is to build a community that reflects the diversity and talent of the continent.

---

📄 License

By contributing, you agree that your contributions will be licensed under the MIT License (for open-source components) or as specified in the NOTICE.md file.

---

🙏 Thank You

Every contribution matters. Whether you fix a typo, add a new model, or spend weeks on a novel fusion mechanism, you are helping advance AI research for African road safety.

"If you want to go fast, go alone. If you want to go far, go together."

— African proverb

---

Happy coding! 🚀

Last updated: 2026


