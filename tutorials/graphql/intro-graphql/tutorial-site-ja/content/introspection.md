---
title: "GraphQLイントロスペクション"
metaTitle: "GraphQLイントロスペクション | GraphQLチュートリアル"
metaDescription: "GraphQLイントロスペクションとは何か、そていGraphiQLなどのコミュニティに関するツールがどのように役立つかを紹介します。"
---

RESTに多くの利点をもたらすGraphQLの主な機能の1つがイントロスペクションです。GraphQLクエリ言語は強く型付けされています。このは強い型付けシステムによって、基本となるスキーマをクエリして理解することができます。

このスキーマはフロントエンドチームとバックエンドチームの間の契約として機能します。しかし、どのようにしてフロントエンド開発者はバックエンドスキーマがどのようなものかを把握するのでしょうか？また、どのようにして過剰な過不足を防ぐのでしょうか？これはイントロスペクションクエリによって可能になります。

## イントロスペクションクエリ {#introspection-queries}

GraphQLサーバーは、同じGraphQLクエリ言語を使って、スキーマに対するイントロスペクションをサポートします。

サーバーは、`Query` 操作タイプで以下のイントロスペクションクエリを公開します。

- `__schema`
- `__type`
- `__typename`

イントロスペクションクエリは `__` で始まることに注意してください。

## コミュニティツール {#community-tooling}

イントロスペクションによって、コミュニティはGraphQLに関する素晴らしいツールを構築できます。[GraphiQL](https://github.com/graphql/graphiql)と[GraphQLプレイグラウンド](https://github.com/prisma-labs/graphql-playground)は、イントロスペクション機能を利用して、開発者にセルフドキュメントを提供して、APIを迅速に試します。

上記のツールは、`__schema` イントロスペクションクエリを使用して、スキーマのドキュメントを与えます。`__schema` クエリを試してさらに検討することで、さまざまな選択セット、フィールド、ディレクティブを確認できます。