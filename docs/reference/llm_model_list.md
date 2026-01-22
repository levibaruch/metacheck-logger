# List LLM Models

List available LLM models for the specified platform.

## Usage

``` r
llm_model_list(platform = NULL)
```

## Arguments

- platform:

  The platform. If NULL, checks all platforms for which you have a valid
  API_KEY.

## Value

a data frame of models and info

## Details

For platforms other than groq, returns the value from the corresponding
ellmer::models_platform function.

## Examples

``` r
# \donttest{
  llm_model_list()
#>          platform                                            id cached_input
#> 1   google_gemini             deep-research-pro-preview-12-2025           NA
#> 2   google_gemini                              gemini-2.0-flash      0.02500
#> 3   google_gemini                          gemini-2.0-flash-001      0.02500
#> 4   google_gemini                          gemini-2.0-flash-exp           NA
#> 5   google_gemini                         gemini-2.0-flash-lite      0.01875
#> 6   google_gemini                     gemini-2.0-flash-lite-001           NA
#> 7   google_gemini                 gemini-2.0-flash-lite-preview           NA
#> 8   google_gemini           gemini-2.0-flash-lite-preview-02-05      0.01875
#> 9   google_gemini       gemini-2.5-computer-use-preview-10-2025           NA
#> 10  google_gemini                              gemini-2.5-flash      0.07500
#> 11  google_gemini                        gemini-2.5-flash-image           NA
#> 12  google_gemini                         gemini-2.5-flash-lite      0.02500
#> 13  google_gemini         gemini-2.5-flash-lite-preview-09-2025      0.02500
#> 14  google_gemini              gemini-2.5-flash-preview-09-2025      0.07500
#> 15  google_gemini                  gemini-2.5-flash-preview-tts      0.03750
#> 16  google_gemini                                gemini-2.5-pro      0.31250
#> 17  google_gemini                    gemini-2.5-pro-preview-tts      0.31250
#> 18  google_gemini                        gemini-3-flash-preview           NA
#> 19  google_gemini                    gemini-3-pro-image-preview           NA
#> 20  google_gemini                          gemini-3-pro-preview           NA
#> 21  google_gemini                               gemini-exp-1206           NA
#> 22  google_gemini                           gemini-flash-latest      0.07500
#> 23  google_gemini                      gemini-flash-lite-latest      0.02500
#> 24  google_gemini                             gemini-pro-latest           NA
#> 25  google_gemini                gemini-robotics-er-1.5-preview           NA
#> 26  google_gemini                                gemma-3-12b-it           NA
#> 27  google_gemini                                 gemma-3-1b-it           NA
#> 28  google_gemini                                gemma-3-27b-it           NA
#> 29  google_gemini                                 gemma-3-4b-it           NA
#> 30  google_gemini                               gemma-3n-e2b-it           NA
#> 31  google_gemini                               gemma-3n-e4b-it           NA
#> 32  google_gemini                       nano-banana-pro-preview           NA
#> 33         openai                                 gpt-5.2-codex           NA
#> 34         openai                          chatgpt-image-latest           NA
#> 35         openai                     gpt-audio-mini-2025-12-15           NA
#> 36         openai                    gpt-4o-mini-tts-2025-12-15           NA
#> 37         openai                  gpt-realtime-mini-2025-12-15           NA
#> 38         openai             gpt-4o-mini-transcribe-2025-12-15           NA
#> 39         openai             gpt-4o-mini-transcribe-2025-03-20           NA
#> 40         openai                    gpt-4o-mini-tts-2025-03-20           NA
#> 41         openai                        gpt-5.2-pro-2025-12-11           NA
#> 42         openai                                   gpt-5.2-pro           NA
#> 43         openai                           gpt-5.2-chat-latest           NA
#> 44         openai                            gpt-5.2-2025-12-11           NA
#> 45         openai                                       gpt-5.2           NA
#> 46         openai                                 gpt-image-1.5           NA
#> 47         openai                             gpt-5.1-codex-max           NA
#> 48         openai                            gpt-5.1-codex-mini           NA
#> 49         openai                                 gpt-5.1-codex           NA
#> 50         openai                            gpt-5.1-2025-11-13           NA
#> 51         openai                                       gpt-5.1           NA
#> 52         openai                           gpt-5.1-chat-latest           NA
#> 53         openai                   gpt-5-search-api-2025-10-14           NA
#> 54         openai                                        sora-2           NA
#> 55         openai                                    sora-2-pro           NA
#> 56         openai                          gpt-5-pro-2025-10-06           NA
#> 57         openai                                     gpt-5-pro           NA
#> 58         openai                                gpt-audio-mini           NA
#> 59         openai                     gpt-audio-mini-2025-10-06           NA
#> 60         openai                              gpt-5-search-api           NA
#> 61         openai                             gpt-realtime-mini           NA
#> 62         openai                  gpt-realtime-mini-2025-10-06           NA
#> 63         openai                              gpt-image-1-mini      0.20000
#> 64         openai                                   gpt-5-codex      0.12500
#> 65         openai                                     gpt-audio           NA
#> 66         openai                          gpt-audio-2025-08-28           NA
#> 67         openai                                  gpt-realtime      0.40000
#> 68         openai                       gpt-realtime-2025-08-28      0.40000
#> 69         openai                                         gpt-5      0.12500
#> 70         openai                         gpt-5-mini-2025-08-07      0.02500
#> 71         openai                                    gpt-5-mini      0.02500
#> 72         openai                         gpt-5-nano-2025-08-07      0.00500
#> 73         openai                                    gpt-5-nano      0.00500
#> 74         openai                             gpt-5-chat-latest      0.12500
#> 75         openai                              gpt-5-2025-08-07      0.12500
#> 76         openai                     gpt-4o-transcribe-diarize           NA
#> 77         openai            gpt-4o-realtime-preview-2025-06-03      2.50000
#> 78         openai               gpt-4o-audio-preview-2025-06-03           NA
#> 79         openai                                   gpt-image-1           NA
#> 80         openai                            gpt-4.1-2025-04-14      0.50000
#> 81         openai                                       gpt-4.1      0.50000
#> 82         openai                       gpt-4.1-mini-2025-04-14      0.10000
#> 83         openai                                  gpt-4.1-mini      0.10000
#> 84         openai                       gpt-4.1-nano-2025-04-14      0.02500
#> 85         openai                                  gpt-4.1-nano      0.02500
#> 86         openai                                            o3      0.50000
#> 87         openai                                       o4-mini      0.27500
#> 88         openai                                 o3-2025-04-16      0.50000
#> 89         openai                            o4-mini-2025-04-16      0.27500
#> 90         openai                               gpt-4o-mini-tts           NA
#> 91         openai                             o1-pro-2025-03-19           NA
#> 92         openai                                        o1-pro           NA
#> 93         openai                             gpt-4o-transcribe           NA
#> 94         openai                        gpt-4o-mini-transcribe           NA
#> 95         openai              gpt-4o-search-preview-2025-03-11      1.25000
#> 96         openai                         gpt-4o-search-preview      1.25000
#> 97         openai         gpt-4o-mini-search-preview-2025-03-11      0.07500
#> 98         openai                    gpt-4o-mini-search-preview      0.07500
#> 99         openai                             gpt-4o-2024-11-20      1.25000
#> 100        openai                            o3-mini-2025-01-31      0.55000
#> 101        openai                                       o3-mini      0.55000
#> 102        openai                                 o1-2024-12-17      7.50000
#> 103        openai                                            o1      7.50000
#> 104        openai                  gpt-4o-mini-realtime-preview      0.30000
#> 105        openai                     gpt-4o-mini-audio-preview           NA
#> 106        openai       gpt-4o-mini-realtime-preview-2024-12-17      0.30000
#> 107        openai          gpt-4o-mini-audio-preview-2024-12-17           NA
#> 108        openai               gpt-4o-audio-preview-2024-12-17           NA
#> 109        openai            gpt-4o-realtime-preview-2024-12-17      2.50000
#> 110        openai                    omni-moderation-2024-09-26           NA
#> 111        openai                        omni-moderation-latest           NA
#> 112        openai                       gpt-4o-realtime-preview      2.50000
#> 113        openai                          gpt-4o-audio-preview           NA
#> 114        openai                             chatgpt-4o-latest           NA
#> 115        openai                             gpt-4o-2024-08-06      1.25000
#> 116        openai                        gpt-4o-mini-2024-07-18      0.07500
#> 117        openai                                   gpt-4o-mini      0.07500
#> 118        openai                                        gpt-4o      1.25000
#> 119        openai                             gpt-4o-2024-05-13           NA
#> 120        openai                        gpt-4-turbo-2024-04-09           NA
#> 121        openai                                   gpt-4-turbo           NA
#> 122        openai                            gpt-4-0125-preview           NA
#> 123        openai                           gpt-4-turbo-preview           NA
#> 124        openai                            gpt-3.5-turbo-0125           NA
#> 125        openai                        text-embedding-3-small           NA
#> 126        openai                        text-embedding-3-large           NA
#> 127        openai                                      tts-1-hd           NA
#> 128        openai                                    tts-1-1106           NA
#> 129        openai                                 tts-1-hd-1106           NA
#> 130        openai                            gpt-4-1106-preview           NA
#> 131        openai                            gpt-3.5-turbo-1106           NA
#> 132        openai                                      dall-e-2           NA
#> 133        openai                                      dall-e-3           NA
#> 134        openai                   gpt-3.5-turbo-instruct-0914           NA
#> 135        openai                        gpt-3.5-turbo-instruct           NA
#> 136        openai                                   davinci-002           NA
#> 137        openai                                   babbage-002           NA
#> 138        openai                                         gpt-4           NA
#> 139        openai                                    gpt-4-0613           NA
#> 140        openai                             gpt-3.5-turbo-16k           NA
#> 141        openai                                         tts-1           NA
#> 142        openai                                 gpt-3.5-turbo           NA
#> 143        openai                                     whisper-1           NA
#> 144        openai                        text-embedding-ada-002           NA
#> 145          groq                            groq/compound-mini           NA
#> 146          groq                                    allam-2-7b           NA
#> 147          groq                                qwen/qwen3-32b           NA
#> 148          groq                            openai/gpt-oss-20b           NA
#> 149          groq                 canopylabs/orpheus-v1-english           NA
#> 150          groq           meta-llama/llama-prompt-guard-2-86m           NA
#> 151          groq                   moonshotai/kimi-k2-instruct           NA
#> 152          groq                          llama-3.1-8b-instant           NA
#> 153          groq meta-llama/llama-4-maverick-17b-128e-instruct           NA
#> 154          groq                                 groq/compound           NA
#> 155          groq                  openai/gpt-oss-safeguard-20b           NA
#> 156          groq               canopylabs/orpheus-arabic-saudi           NA
#> 157          groq                  meta-llama/llama-guard-4-12b           NA
#> 158          groq           meta-llama/llama-prompt-guard-2-22m           NA
#> 159          groq     meta-llama/llama-4-scout-17b-16e-instruct           NA
#> 160          groq                       llama-3.3-70b-versatile           NA
#> 161          groq                           openai/gpt-oss-120b           NA
#> 162          groq              moonshotai/kimi-k2-instruct-0905           NA
#>       input output created_at        owned_by object context_window
#> 1        NA     NA       <NA>            <NA>   <NA>             NA
#> 2     0.100    0.4       <NA>            <NA>   <NA>             NA
#> 3     0.100    0.4       <NA>            <NA>   <NA>             NA
#> 4        NA     NA       <NA>            <NA>   <NA>             NA
#> 5     0.075    0.3       <NA>            <NA>   <NA>             NA
#> 6        NA     NA       <NA>            <NA>   <NA>             NA
#> 7        NA     NA       <NA>            <NA>   <NA>             NA
#> 8     0.075    0.3       <NA>            <NA>   <NA>             NA
#> 9        NA     NA       <NA>            <NA>   <NA>             NA
#> 10    0.300    2.5       <NA>            <NA>   <NA>             NA
#> 11       NA     NA       <NA>            <NA>   <NA>             NA
#> 12    0.100    0.4       <NA>            <NA>   <NA>             NA
#> 13    0.100    0.4       <NA>            <NA>   <NA>             NA
#> 14    0.300    2.5       <NA>            <NA>   <NA>             NA
#> 15    0.150    0.6       <NA>            <NA>   <NA>             NA
#> 16    1.250   10.0       <NA>            <NA>   <NA>             NA
#> 17    1.250   10.0       <NA>            <NA>   <NA>             NA
#> 18       NA     NA       <NA>            <NA>   <NA>             NA
#> 19       NA     NA       <NA>            <NA>   <NA>             NA
#> 20       NA     NA       <NA>            <NA>   <NA>             NA
#> 21       NA     NA       <NA>            <NA>   <NA>             NA
#> 22    0.300    2.5       <NA>            <NA>   <NA>             NA
#> 23    0.100    0.4       <NA>            <NA>   <NA>             NA
#> 24       NA     NA       <NA>            <NA>   <NA>             NA
#> 25       NA     NA       <NA>            <NA>   <NA>             NA
#> 26       NA     NA       <NA>            <NA>   <NA>             NA
#> 27       NA     NA       <NA>            <NA>   <NA>             NA
#> 28       NA     NA       <NA>            <NA>   <NA>             NA
#> 29       NA     NA       <NA>            <NA>   <NA>             NA
#> 30       NA     NA       <NA>            <NA>   <NA>             NA
#> 31       NA     NA       <NA>            <NA>   <NA>             NA
#> 32       NA     NA       <NA>            <NA>   <NA>             NA
#> 33       NA     NA 2025-12-19          system   <NA>             NA
#> 34       NA     NA 2025-12-16          system   <NA>             NA
#> 35       NA     NA 2025-12-15          system   <NA>             NA
#> 36       NA     NA 2025-12-13          system   <NA>             NA
#> 37       NA     NA 2025-12-13          system   <NA>             NA
#> 38       NA     NA 2025-12-13          system   <NA>             NA
#> 39       NA     NA 2025-12-13          system   <NA>             NA
#> 40       NA     NA 2025-12-13          system   <NA>             NA
#> 41       NA     NA 2025-12-10          system   <NA>             NA
#> 42       NA     NA 2025-12-10          system   <NA>             NA
#> 43       NA     NA 2025-12-10          system   <NA>             NA
#> 44       NA     NA 2025-12-09          system   <NA>             NA
#> 45       NA     NA 2025-12-09          system   <NA>             NA
#> 46       NA     NA 2025-11-25          system   <NA>             NA
#> 47       NA     NA 2025-11-20          system   <NA>             NA
#> 48       NA     NA 2025-11-13          system   <NA>             NA
#> 49       NA     NA 2025-11-12          system   <NA>             NA
#> 50       NA     NA 2025-11-10          system   <NA>             NA
#> 51       NA     NA 2025-11-10          system   <NA>             NA
#> 52       NA     NA 2025-11-07          system   <NA>             NA
#> 53       NA     NA 2025-10-09          system   <NA>             NA
#> 54       NA     NA 2025-10-05          system   <NA>             NA
#> 55       NA     NA 2025-10-05          system   <NA>             NA
#> 56   15.000  120.0 2025-10-03          system   <NA>             NA
#> 57   15.000  120.0 2025-10-03          system   <NA>             NA
#> 58       NA     NA 2025-10-03          system   <NA>             NA
#> 59       NA     NA 2025-10-03          system   <NA>             NA
#> 60       NA     NA 2025-10-03          system   <NA>             NA
#> 61    0.600    2.4 2025-10-03          system   <NA>             NA
#> 62       NA     NA 2025-10-03          system   <NA>             NA
#> 63    2.000     NA 2025-09-26          system   <NA>             NA
#> 64    1.250   10.0 2025-09-10          system   <NA>             NA
#> 65       NA     NA 2025-08-28          system   <NA>             NA
#> 66       NA     NA 2025-08-27          system   <NA>             NA
#> 67    4.000   16.0 2025-08-27          system   <NA>             NA
#> 68    4.000   16.0 2025-08-27          system   <NA>             NA
#> 69    1.250   10.0 2025-08-05          system   <NA>             NA
#> 70    0.250    2.0 2025-08-05          system   <NA>             NA
#> 71    0.250    2.0 2025-08-05          system   <NA>             NA
#> 72    0.050    0.4 2025-08-05          system   <NA>             NA
#> 73    0.050    0.4 2025-08-05          system   <NA>             NA
#> 74    1.250   10.0 2025-08-01          system   <NA>             NA
#> 75    1.250   10.0 2025-08-01          system   <NA>             NA
#> 76       NA     NA 2025-06-24          system   <NA>             NA
#> 77    5.000   20.0 2025-06-02          system   <NA>             NA
#> 78    2.500   10.0 2025-06-02          system   <NA>             NA
#> 79       NA     NA 2025-04-24          system   <NA>             NA
#> 80    2.000    8.0 2025-04-10          system   <NA>             NA
#> 81    2.000    8.0 2025-04-10          system   <NA>             NA
#> 82    0.400    1.6 2025-04-10          system   <NA>             NA
#> 83    0.400    1.6 2025-04-10          system   <NA>             NA
#> 84    0.100    0.4 2025-04-10          system   <NA>             NA
#> 85    0.100    0.4 2025-04-10          system   <NA>             NA
#> 86    2.000    8.0 2025-04-09          system   <NA>             NA
#> 87    1.100    4.4 2025-04-09          system   <NA>             NA
#> 88    2.000    8.0 2025-04-08          system   <NA>             NA
#> 89    1.100    4.4 2025-04-08          system   <NA>             NA
#> 90    2.500   10.0 2025-03-19          system   <NA>             NA
#> 91  150.000  600.0 2025-03-17          system   <NA>             NA
#> 92  150.000  600.0 2025-03-17          system   <NA>             NA
#> 93    2.500   10.0 2025-03-15          system   <NA>             NA
#> 94    1.250    5.0 2025-03-15          system   <NA>             NA
#> 95    2.500   10.0 2025-03-07          system   <NA>             NA
#> 96    2.500   10.0 2025-03-07          system   <NA>             NA
#> 97    0.150    0.6 2025-03-07          system   <NA>             NA
#> 98    0.150    0.6 2025-03-07          system   <NA>             NA
#> 99    2.500   10.0 2025-02-12          system   <NA>             NA
#> 100   1.100    4.4 2025-01-27          system   <NA>             NA
#> 101   1.100    4.4 2025-01-17          system   <NA>             NA
#> 102  15.000   60.0 2024-12-16          system   <NA>             NA
#> 103  15.000   60.0 2024-12-16          system   <NA>             NA
#> 104   0.600    2.4 2024-12-16          system   <NA>             NA
#> 105   0.150    0.6 2024-12-16          system   <NA>             NA
#> 106   0.600    2.4 2024-12-13          system   <NA>             NA
#> 107   0.150    0.6 2024-12-13          system   <NA>             NA
#> 108   2.500   10.0 2024-12-12          system   <NA>             NA
#> 109   5.000   20.0 2024-12-11          system   <NA>             NA
#> 110      NA     NA 2024-11-27          system   <NA>             NA
#> 111      NA     NA 2024-11-15          system   <NA>             NA
#> 112   5.000   20.0 2024-09-30          system   <NA>             NA
#> 113   2.500   10.0 2024-09-27          system   <NA>             NA
#> 114   5.000   15.0 2024-08-13          system   <NA>             NA
#> 115   2.500   10.0 2024-08-04          system   <NA>             NA
#> 116   0.150    0.6 2024-07-16          system   <NA>             NA
#> 117   0.150    0.6 2024-07-16          system   <NA>             NA
#> 118   2.500   10.0 2024-05-10          system   <NA>             NA
#> 119   5.000   15.0 2024-05-10          system   <NA>             NA
#> 120  10.000   30.0 2024-04-08          system   <NA>             NA
#> 121  10.000   30.0 2024-04-05          system   <NA>             NA
#> 122  10.000   30.0 2024-01-23          system   <NA>             NA
#> 123  10.000   30.0 2024-01-23          system   <NA>             NA
#> 124   0.500    1.5 2024-01-23          system   <NA>             NA
#> 125   0.020    0.0 2024-01-22          system   <NA>             NA
#> 126   0.130    0.0 2024-01-22          system   <NA>             NA
#> 127      NA     NA 2023-11-03          system   <NA>             NA
#> 128      NA     NA 2023-11-03          system   <NA>             NA
#> 129      NA     NA 2023-11-03          system   <NA>             NA
#> 130  10.000   30.0 2023-11-02          system   <NA>             NA
#> 131   1.000    2.0 2023-11-02          system   <NA>             NA
#> 132      NA     NA 2023-11-01          system   <NA>             NA
#> 133      NA     NA 2023-10-31          system   <NA>             NA
#> 134      NA     NA 2023-09-07          system   <NA>             NA
#> 135      NA     NA 2023-08-24          system   <NA>             NA
#> 136      NA     NA 2023-08-21          system   <NA>             NA
#> 137      NA     NA 2023-08-21          system   <NA>             NA
#> 138  30.000   60.0 2023-06-27          openai   <NA>             NA
#> 139  30.000   60.0 2023-06-12          openai   <NA>             NA
#> 140   3.000    4.0 2023-05-10 openai-internal   <NA>             NA
#> 141      NA     NA 2023-04-19 openai-internal   <NA>             NA
#> 142   0.500    1.5 2023-02-28          openai   <NA>             NA
#> 143      NA     NA 2023-02-27 openai-internal   <NA>             NA
#> 144   0.100    0.0 2022-12-16 openai-internal   <NA>             NA
#> 145      NA     NA 2025-09-04            Groq  model         131072
#> 146      NA     NA 2025-01-23           SDAIA  model           4096
#> 147      NA     NA 2025-05-28   Alibaba Cloud  model         131072
#> 148      NA     NA 2025-08-05          OpenAI  model         131072
#> 149      NA     NA 2025-12-20     Canopy Labs  model           4000
#> 150      NA     NA 2025-05-30            Meta  model            512
#> 151      NA     NA 2025-07-13     Moonshot AI  model         131072
#> 152      NA     NA 2023-09-03            Meta  model         131072
#> 153      NA     NA 2025-04-05            Meta  model         131072
#> 154      NA     NA 2025-09-04            Groq  model         131072
#> 155      NA     NA 2025-10-29          OpenAI  model         131072
#> 156      NA     NA 2025-12-17     Canopy Labs  model           4000
#> 157      NA     NA 2025-05-09            Meta  model         131072
#> 158      NA     NA 2025-05-30            Meta  model            512
#> 159      NA     NA 2025-04-05            Meta  model         131072
#> 160      NA     NA 2024-12-06            Meta  model         131072
#> 161      NA     NA 2025-08-05          OpenAI  model         131072
#> 162      NA     NA 2025-09-05     Moonshot AI  model         262144
#>     max_completion_tokens
#> 1                      NA
#> 2                      NA
#> 3                      NA
#> 4                      NA
#> 5                      NA
#> 6                      NA
#> 7                      NA
#> 8                      NA
#> 9                      NA
#> 10                     NA
#> 11                     NA
#> 12                     NA
#> 13                     NA
#> 14                     NA
#> 15                     NA
#> 16                     NA
#> 17                     NA
#> 18                     NA
#> 19                     NA
#> 20                     NA
#> 21                     NA
#> 22                     NA
#> 23                     NA
#> 24                     NA
#> 25                     NA
#> 26                     NA
#> 27                     NA
#> 28                     NA
#> 29                     NA
#> 30                     NA
#> 31                     NA
#> 32                     NA
#> 33                     NA
#> 34                     NA
#> 35                     NA
#> 36                     NA
#> 37                     NA
#> 38                     NA
#> 39                     NA
#> 40                     NA
#> 41                     NA
#> 42                     NA
#> 43                     NA
#> 44                     NA
#> 45                     NA
#> 46                     NA
#> 47                     NA
#> 48                     NA
#> 49                     NA
#> 50                     NA
#> 51                     NA
#> 52                     NA
#> 53                     NA
#> 54                     NA
#> 55                     NA
#> 56                     NA
#> 57                     NA
#> 58                     NA
#> 59                     NA
#> 60                     NA
#> 61                     NA
#> 62                     NA
#> 63                     NA
#> 64                     NA
#> 65                     NA
#> 66                     NA
#> 67                     NA
#> 68                     NA
#> 69                     NA
#> 70                     NA
#> 71                     NA
#> 72                     NA
#> 73                     NA
#> 74                     NA
#> 75                     NA
#> 76                     NA
#> 77                     NA
#> 78                     NA
#> 79                     NA
#> 80                     NA
#> 81                     NA
#> 82                     NA
#> 83                     NA
#> 84                     NA
#> 85                     NA
#> 86                     NA
#> 87                     NA
#> 88                     NA
#> 89                     NA
#> 90                     NA
#> 91                     NA
#> 92                     NA
#> 93                     NA
#> 94                     NA
#> 95                     NA
#> 96                     NA
#> 97                     NA
#> 98                     NA
#> 99                     NA
#> 100                    NA
#> 101                    NA
#> 102                    NA
#> 103                    NA
#> 104                    NA
#> 105                    NA
#> 106                    NA
#> 107                    NA
#> 108                    NA
#> 109                    NA
#> 110                    NA
#> 111                    NA
#> 112                    NA
#> 113                    NA
#> 114                    NA
#> 115                    NA
#> 116                    NA
#> 117                    NA
#> 118                    NA
#> 119                    NA
#> 120                    NA
#> 121                    NA
#> 122                    NA
#> 123                    NA
#> 124                    NA
#> 125                    NA
#> 126                    NA
#> 127                    NA
#> 128                    NA
#> 129                    NA
#> 130                    NA
#> 131                    NA
#> 132                    NA
#> 133                    NA
#> 134                    NA
#> 135                    NA
#> 136                    NA
#> 137                    NA
#> 138                    NA
#> 139                    NA
#> 140                    NA
#> 141                    NA
#> 142                    NA
#> 143                    NA
#> 144                    NA
#> 145                  8192
#> 146                  4096
#> 147                 40960
#> 148                 65536
#> 149                 50000
#> 150                   512
#> 151                 16384
#> 152                131072
#> 153                  8192
#> 154                  8192
#> 155                 65536
#> 156                 50000
#> 157                  1024
#> 158                   512
#> 159                  8192
#> 160                 32768
#> 161                 65536
#> 162                 16384
# }
```
