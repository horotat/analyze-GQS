# Godspeed Questionnaire Analysis in R

This R script calculates the mean scores and Cronbach's alpha for different dimensions of the Godspeed Questionnaire, which is used to assess user perceptions of robots or other interactive technologies.

## Table of Contents

- [Getting Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Data Format](#data-format)
- [Running the Script](#running-the-script)
- [Interpretation of Results](#interpretation-of-results)
- [License](#license)

## Getting Started

To use this script, you will need to have your data formatted correctly in a data frame named `gs`. The script will calculate the average score and Cronbach's alpha for each of the Godspeed Questionnaire's dimensions: Anthropomorphism, Animacy, Likeability, Intelligence, and Safety.

## Prerequisites

- R (version 4.0.0 or later)
- R packages: `dplyr`, `psych`

You can install the required R packages by running:

```r
install.packages("dplyr")
install.packages("psych")
```

## Data Format

The `gs` data frame should contain the following columns:

1. **Participant Information Columns**: These may include `id`, `age`, `gender`, etc.
2. **Godspeed Questions Columns**: The responses to each Godspeed question should be stored in separate columns with the following names:

   - **Anthropomorphism**:
     - `Fake.Natural`
     - `Machinelike.Humanlike`
     - `Unconscious.Conscious`
     - `Artificial.Lifelike`
     - `Moving.rigidly.Moving.elegantly`
   - **Animacy**:
     - `Dead.Alive`
     - `Stagnant.Lively`
     - `Mechanical.Organic`
     - `Artificial.Lifelike`
     - `Inert.Interactive`
     - `Apathetic.Responsive`
   - **Likeability**:
     - `Dislike.Like`
     - `Unfriendly.Friendly`
     - `Unkind.Kind`
     - `Unpleasant.Pleasant`
     - `Awful.Nice`
   - **Intelligence**:
     - `Incompetent.Competent`
     - `Ignorant.Knowledgeable`
     - `Irresponsible.Responsible`
     - `Unintelligent.Intelligent`
     - `Foolish.Sensible`
   - **Safety**:
     - `Anxious.Relaxed`
     - `Agitated.Calm`
     - `Surprised.Still`

### Example Data Frame Structure

Below is an example of how your `gs` data frame might look:

| id  | age | gender | Fake.Natural | Machinelike.Humanlike | Unconscious.Conscious | ... | Surprised.Still |
|-----|-----|--------|--------------|-----------------------|-----------------------|-----|-----------------|
| 1   | 25  | Male   | 5            | 4                     | 3                     | ... | 2               |
| 2   | 30  | Female | 4            | 5                     | 4                     | ... | 3               |
| ... | ... | ...    | ...          | ...                   | ...                   | ... | ...             |

## Running the Script

1. Ensure your data is loaded into an R data frame named `gs`.
2. Run the script in R

## Interpretation of Results

- **Mean Scores**: The mean score for each Godspeed dimension provides an overall measure of how participants perceive the robot or technology in that dimension.
- **Cronbach's Alpha**: This statistic measures the internal consistency of the responses within each dimension. A value of 0.7 or higher typically indicates acceptable reliability.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
