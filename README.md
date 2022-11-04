# kover-build-explosion

# Without Kover

```bash
./gradlew clean testSweetDebugUnitTest | grep -E "> Task :app:(compile.+Kotlin|test)|actionable"
> Task :app:compileSweetDebugKotlin
> Task :app:compileSweetDebugUnitTestKotlin
> Task :app:testSweetDebugUnitTest
23 actionable tasks: 23 executed
```

# WITH Kover

```bash
./gradlew clean testSweetDebugUnitTest koverXmlReport | grep -E "> Task :app:(compile.+Kotlin|test)|actionable"
> Task :app:compileSaltyDebugKotlin
> Task :app:compileSaltyDebugUnitTestKotlin
> Task :app:compileSweetDebugKotlin
> Task :app:testSaltyDebugUnitTest
> Task :app:compileSweetDebugUnitTestKotlin
> Task :app:testSweetDebugUnitTest
> Task :app:compileSweetReleaseKotlin
> Task :app:compileSweetReleaseUnitTestKotlin
> Task :app:compileSaltyReleaseKotlin
> Task :app:testSweetReleaseUnitTest
> Task :app:compileSaltyReleaseUnitTestKotlin
> Task :app:testSaltyReleaseUnitTest
91 actionable tasks: 91 executed
```
