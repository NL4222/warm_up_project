# warm_up_project
## Name : 劉千慈

* About throughputs , please record the Tokens / Sec of Eval Time 

### Basic Challenge
| Throughputs (Tokens/sec) | CPU      | GPU      | 
| --------                 | -------- | -------- | 
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf  |11.60     | 80.66   |


### Medium Challenge
| Throughputs (Tokens/sec) | CPU      | GPU      | 
| --------                 | -------- | -------- | 
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf  | XXXX     | XXXX     |
| TinyLlama-1.1B-Chat-v1.0-f16  | XXXX     | XXXX     |



### Advance Challenge
| Throughputs (Tokens/sec) | CPU      | GPU      | 
| --------                 | -------- | -------- | 
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf  | XXXX     | XXXX     |
| TinyLlama-1.1B-Chat-v1.0-f16  | XXXX     | XXXX     |
| TinyLlama-1.1B-Chat-v1.0-Q8  | XXXX     | XXXX     |


### Advance Challenge

|                           | Accuracy  |
| --------                 | --------  |
| tinyllama-1.1b-chat-v0.3.Q4_K_M.gguf | x/10     |
| TinyLlama-1.1B-Chat-v1.0-f16         | x/10     |
| TinyLlama-1.1B-Chat-v1.0-Q8          | x/10     |

### Questions
* What problems you encountered? How you solve it?  
   Firstly, I want to use the GPU, however, I set the make only use LLAMA_CUDA.
  And the error message say that I need to use LIBCURL. I try many times and all get the similar error message.
  Then, I check the sample code in hugging face, I find that it's CURL, not LIBCURL.
* What you observed between CPU / GPU performance ?  
  By observation, we can find that the Tokens / Sec of Eval Time in GPU is better than CPU.
  All tasks, ex: load, sample, prompt eval and eval, GPU can save much time than CPU.
  The time that CPU use is about ten times as longer as GPU.   
  
* Will quantization or smaller-parameters model impact model accuracy or inference throughput ? If so , what's the variation?  
  Although I didn't complete the part, I think both of them impact the model accuracy and throughput.  
  Quantization and smaller-parameter are both reduce the accuracy, but both of them get greater throughput.  
  Because the Quantization may represent the detail in modeal not well, the accuracy will decrease. However, the thoughput will be faster.  
  As the same token in  smaller-parameter, it decrease the parameter, also decrease the ability to learn complex condition.  


