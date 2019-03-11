---
title: Application Unit Test
permalink: /editor/application-unit-test
layout: default
---

# Application Unit Test
ResInsight has several application unit tests located in the `ApplicationCode/UnitTests` folder.

## Test datasets
Files used by the unit tests can be stored in the folder `ApplicationCode/UnitTests/TestData`

To use the data here, use the define **TEST_DATA_DIR** before appending the specific folder used in the test.

`QString testDataRootFolder = QString("%1/ParsingOfDataKeywords/").arg(TEST_DATA_DIR);\ `
