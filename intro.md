在实践中，给定相同的查询、键和值集合，我们可能希望我们的模型将来自同一注意力机制不同行为的知识结合起来，
例如在一个序列中捕获不同范围 (例如，较短范围与较长范围) 的依赖关系。因此，允许我们的注意力机制共同使用查询、键和值的不同表示子空间可能是有益的。

Multi-Head Attention 是由多个 Self-Attention 组合形成的。对于同一个文本，一个Attention获得一个表示空间，如果多个Attention，
则可以获得多个不同的表示空间。基于这种想法，就有了Multi-Head Attention。换句话说，Multi-Head Attention为Attention提供了多个“representation subspaces”。
因为在每个Attention中，采用不同的Query / Key / Value权重矩阵，每个矩阵都是随机初始化生成的。然后通过训练，将词嵌入投影到不同的“representation subspaces（表示子空间）”中。 
