---
title: '&lt;type_traits&gt;'
ms.date: 11/04/2016
f1_keywords:
- <type_traits>
helpviewer_keywords:
- typetrait header
- type_traits
ms.assetid: 2260b51f-8160-4c66-a82f-00b534cb60d4
ms.openlocfilehash: f56334cbb25132d45dfabb68cbcd5b832096a87c
ms.sourcegitcommit: 6052185696adca270bc9bdbec45a626dd89cdcdd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "50514683"
---
# <a name="lttypetraitsgt"></a>&lt;type_traits&gt;

型引数のプロパティに関する情報を提供する、または変換された型を生成する、コンパイル時定数を備えたテンプレートを定義します。

## <a name="syntax"></a>構文

```cpp
#include <type_traits>
```

## <a name="remarks"></a>Remarks

クラスとテンプレートは、 \<type_traits > 型の推定、分類、および種類関連のエラーを検出して、ジェネリック コードを最適化するため、コンパイル時に変換をサポートするために使用されます。 これらのクラスとテンプレートには、型のプロパティについて記述する単項の型の特徴、型間の関係を記述する二項の型の特徴、および型のプロパティを変更する変換の特徴が含まれます。

型の特徴をサポートするために、ヘルパー クラス `integral_constant` が定義されています。 これには、型の述語の基底クラスを形成するテンプレート特殊化 `true_type` と `false_type` があります。 *型の述語*は、1 つ以上の型引数を受け取るテンプレートです。 型の述語が *true を保持*する場合は、[true_type](../standard-library/type-traits-typedefs.md#true_type) からパブリックに (直接または間接的に) 派生されます。 型の述語が *false を保持*する場合は、[false_type](../standard-library/type-traits-typedefs.md#false_type) からパブリックに (直接または間接的に) 派生されます。

*型修飾子*または*変換の特徴*は、1 つ以上のテンプレート引数を受け取り、変更された型のシノニムである 1 つのメンバー、`type` を持つテンプレートです。

### <a name="alias-templates"></a>エイリアス テンプレート

型の特徴の式を簡略化するために、`typename some_trait<T>::type` の[エイリアス テンプレート](../cpp/aliases-and-typedefs-cpp.md)が提供されます。" `some_trait`" はテンプレート クラス名です。 たとえば、[add_const](../standard-library/add-const-class.md) には、その型 `add_const_t` のエイリアス テンプレートがあり、次のように定義されています。

```cpp
template <class T>
using add_const_t = typename add_const<T>::type;
```

|||||
|-|-|-|-|
|add_const_t|aligned_storage_t|make_signed_t|remove_pointer_t|
|add_cv_t|aligned_union_t|make_unsigned_t|remove_reference_t|
|add_lvalue_reference_t|common_type_t|remove_all_extents_t|remove_volatile_t|
|add_pointer_t|conditional_t|remove_const_t|result_of_t|
|add_rvalue_reference_t|decay_t|remove_cv_t|underlying_type_t|
|add_volatile_t|enable_if_t|remove_extent_t||

### <a name="classes"></a>クラス

ヘルパー クラスと typedef

|||
|-|-|
|[integral_constant](../standard-library/integral-constant-class-bool-constant-class.md)|型および値から整数定数を作成します。|
|[true_type](../standard-library/type-traits-typedefs.md#true_type)|true 値を持つ整数定数を保持します。|
|[false_type](../standard-library/type-traits-typedefs.md#false_type)|false 値を持つ整数定数を保持します。|

主な型のカテゴリ

|||
|-|-|
|[is_void](../standard-library/is-void-class.md)|型があるかどうかをテスト**void**します。|
|[is_null_pointer](../standard-library/is-null-pointer-class.md)|型が `std::nullptr_t` であるかどうかをテストします。|
|[is_integral](../standard-library/is-integral-class.md)|型が整数型であるかどうかをテストします。|
|[is_floating_point](../standard-library/is-floating-point-class.md)|型が浮動小数点型であるかどうかをテストします。|
|[is_array](../standard-library/is-array-class.md)|型が配列型であるかどうかをテストします。|
|[is_pointer](../standard-library/is-pointer-class.md)|型がポインターであるかどうかをテストします。|
|[is_lvalue_reference](../standard-library/is-lvalue-reference-class.md)|型が左辺値参照かどうかをテストします。|
|[is_rvalue_reference](../standard-library/is-rvalue-reference-class.md)|型が右辺値参照かどうかをテストします。|
|[is_member_object_pointer](../standard-library/is-member-object-pointer-class.md)|型がメンバー オブジェクトへのポインターであるかどうかをテストします。|
|[is_member_function_pointer](../standard-library/is-member-function-pointer-class.md)|型がメンバー関数へのポインターであるかどうかをテストします。|
|[is_enum](../standard-library/is-enum-class.md)|型が列挙型であるかどうかをテストします。|
|[is_union](../standard-library/is-union-class.md)|型が共用体であるかどうかをテストします。|
|[is_class](../standard-library/is-class-class.md)|型がクラスであるかどうかをテストします。|
|[is_function](../standard-library/is-function-class.md)|型が関数型であるかどうかをテストします。|

複合型のカテゴリ

|||
|-|-|
|[is_reference](../standard-library/is-reference-class.md)|型が参照であるかどうかをテストします。|
|[is_arithmetic](../standard-library/is-arithmetic-class.md)|型が演算型であるかどうかをテストします。|
|[is_fundamental](../standard-library/is-fundamental-class.md)|型があるかどうかをテスト**void**や演算。|
|[is_object](../standard-library/is-object-class.md)|型がオブジェクト型であるかどうかをテストします。|
|[is_scalar](../standard-library/is-scalar-class.md)|型がスカラーであるかどうかをテストします。|
|[is_compound](../standard-library/is-compound-class.md)|型が非スカラーであるかどうかをテストします。|
|[is_member_pointer](../standard-library/is-member-pointer-class.md)|型がメンバーへのポインターであるかどうかをテストします。|

型のプロパティ

|||
|-|-|
|[is_const](../standard-library/is-const-class.md)|型があるかどうかをテスト**const**します。|
|[is_volatile](../standard-library/is-volatile-class.md)|型があるかどうかをテスト**揮発性**します。|
|[is_trivial](../standard-library/is-trivial-class.md)|型が単純であるかどうかをテストします。|
|[is_trivially_copyable](../standard-library/is-trivially-copyable-class.md)|型が普通にコピー可能であるかどうかをテストします。|
|[is_standard_layout](../standard-library/is-standard-layout-class.md)|型が標準レイアウト型であるかどうかをテストします。|
|[is_pod](../standard-library/is-pod-class.md)|型が POD であるかどうかをテストします。|
|[is_literal_type](../standard-library/is-literal-type-class.md)|型が、`constexpr` 変数にしたり、`constexpr` 関数で使用したりできるかどうかをテストします。|
|[is_empty](../standard-library/is-empty-class.md)|型が空のクラスであるかどうかをテストします。|
|[is_polymorphic](../standard-library/is-polymorphic-class.md)|型がポリモーフィックなクラスであるかどうかをテストします。|
|[is_abstract](../standard-library/is-abstract-class.md)|型が抽象クラスであるかどうかをテストします。|
|[is_final](../standard-library/is-final-class.md)|型が `final` とマークされるクラス型であるかどうかをテストします。|
|[is_signed](../standard-library/is-signed-class.md)|型が符号付き整数であるかどうかをテストします。|
|[is_unsigned](../standard-library/is-unsigned-class.md)|型が符号なし整数であるかどうかをテストします。|
|[is_constructible](../standard-library/is-constructible-class.md)|型が、指定された引数の型を使用して構築できるかどうかをテストします。|
|[is_default_constructible](../standard-library/type-traits-functions.md#is_default_constructible)|型に既定コンストラクターが存在するかどうかをテストします。|
|[is_copy_constructible](../standard-library/type-traits-functions.md#is_copy_constructible)|型にコピー コンストラクターが存在するかどうかをテストします。|
|[is_move_constructible](../standard-library/type-traits-functions.md#is_move_constructible)|型に移動コンストラクターが存在するかどうかをテストします。|
|[is_assignable](../standard-library/type-traits-functions.md#is_assignable)|最初の型に 2 番目の型の値を割り当てることができるかどうかをテストします。|
|[is_copy_assignable](../standard-library/type-traits-functions.md#is_copy_assignable)|型に、その型の const 参照値を割り当てることができるかどうかをテストします。|
|[is_move_assignable](../standard-library/type-traits-functions.md#is_move_assignable)|型に、その型の rvalue 参照を割り当てることができるかどうかをテストします。|
|[is_destructible](../standard-library/is-destructible-class.md)|型が破棄可能かどうかをテストします。|
|[is_trivially_constructible](../standard-library/is-trivially-constructible-class.md)|型が、指定された型を使用して作成されるときに、重要な操作を使用しないかどうかをテストします。|
|[is_trivially_default_constructible](../standard-library/is-trivially-default-constructible-class.md)|型が、既定で作成されるときに、重要な操作を使用しないかどうかをテストします。|
|[is_trivially_copy_constructible](../standard-library/is-trivially-copy-constructible-class.md)|型が、コピーで作成されるときに、重要な操作を使用しないかどうかをテストします。|
|[is_trivially_move_constructible](../standard-library/type-traits-functions.md#is_trivially_move_constructible)|型が、移動で作成されるときに、重要な操作を使用しないかどうかをテストします。|
|[is_trivially_assignable](../standard-library/is-trivially-assignable-class.md)|型が割り当て可能で、かつ割り当てで重要な操作を使用しないかどうかをテストします。|
|[is_trivially_copy_assignable](../standard-library/type-traits-functions.md#is_trivially_copy_assignable)|型が、コピー割り当て可能で、かつ割り当てで重要な操作を使用しないかどうかをテストします。|
|[is_trivially_move_assignable](../standard-library/type-traits-functions.md#is_trivially_move_assignable)|型が、移動で割り当て可能で、かつ割り当てで重要な操作を使用しないかどうかをテストします。|
|[is_trivially_destructible](../standard-library/is-trivially-destructible-class.md)|型が破棄可能で、かつデストラクターが重要な操作を使用しないかどうかをテストします。|
|[is_nothrow_constructible](../standard-library/is-nothrow-constructible-class.md)|型が構築可能で、指定された型を使用して構築されたときにスローしないと判明しているかどうかをテストします。|
|[is_nothrow_default_constructible](../standard-library/is-nothrow-default-constructible-class.md)|型が、既定で構築可能で、既定で構築されたときにスローしないと判明しているかどうかをテストします。|
|[is_nothrow_copy_constructible](../standard-library/is-nothrow-copy-constructible-class.md)|型が、コピーで構築可能で、コピー コンストラクターがスローしないと判明しているかどうかをテストします。|
|[is_nothrow_move_constructible](../standard-library/is-nothrow-move-constructible-class.md)|型が、移動で構築可能で、移動コンストラクターがスローしないと判明しているかどうかをテストします。|
|[is_nothrow_assignable](../standard-library/is-nothrow-assignable-class.md)|型が、指定された型を使用して割り当て可能で、割り当てがスローしないと判明しているかどうかをテストします。|
|[is_nothrow_copy_assignable](../standard-library/is-nothrow-copy-assignable-class.md)|型が、コピーで割り当て可能で、割り当てがスローしないと判明しているかどうかをテストします。|
|[is_nothrow_move_assignable](../standard-library/type-traits-functions.md#is_nothrow_move_assignable)|型が、移動で割り当て可能で、割り当てがスローしないと判明しているかどうかをテストします。|
|[is_nothrow_destructible](../standard-library/is-nothrow-destructible-class.md)|型が破棄可能で、デストラクターがスローしないと判明しているかどうかをテストします。|
|`has_virtual_destructor`|型に仮想デストラクターが存在するかどうかをテストします。|

型プロパティのクエリ

|||
|-|-|
|[alignment_of](../standard-library/alignment-of-class.md)|型のアラインメントを取得します。|
|[rank](../standard-library/rank-class.md)|配列の次元数を取得します。|
|[extent](../standard-library/extent-class.md)|指定した次元にある要素の数を取得します。|

型の関係

|||
|-|-|
|[is_same](../standard-library/is-same-class.md)|2 つの型が等しいかどうかをテストします。|
|[is_base_of](../standard-library/is-base-of-class.md)|一方の型がもう一方の型に基づいているかどうかをテストします。|
|[is_convertible](../standard-library/is-convertible-class.md)|一方の型をもう一方の型に変換できるかどうかをテストします。|

const/volatile の変更

|||
|-|-|
|[add_const](../standard-library/add-const-class.md)|生成、 **const**型からの型。|
|[add_volatile](../standard-library/add-volatile-class.md)|生成、**揮発性**型からの型。|
|[add_cv](../standard-library/add-cv-class.md)|生成、 **const volatile**型からの型。|
|[remove_const](../standard-library/remove-const-class.md)|型から非 const 型を生成します。|
|[remove_volatile](../standard-library/remove-volatile-class.md)|型から非 volatile 型を生成します。|
|[remove_cv](../standard-library/remove-cv-class.md)|型から非 const の非 volatile 型を生成します。|

参照の変更

|||
|-|-|
|[add_lvalue_reference](../standard-library/add-lvalue-reference-class.md)|型から型への参照を生成します。|
|[add_rvalue_reference](../standard-library/add-rvalue-reference-class.md)|型から型への rvalue 参照を生成します。|
|[remove_reference](../standard-library/remove-reference-class.md)|型から非参照型を生成します。|

符号の変更

|||
|-|-|
|[make_signed](../standard-library/make-signed-class.md)|符号付きの場合は型を生成し、サイズが型以上の型または最小の符号付きの型を生成します。|
|[make_unsigned](../standard-library/make-unsigned-class.md)|符号なしの場合は型を生成し、サイズが型以上の型または最小の符号なしの型を生成します。|

配列の変更

|||
|-|-|
|[remove_all_extents](../standard-library/remove-all-extents-class.md)|配列型から非配列型を生成します。|
|[remove_extent](../standard-library/remove-extent-class.md)|配列型から要素型を生成します。|

ポインターの変更

|||
|-|-|
|[add_pointer](../standard-library/add-pointer-class.md)|型から型へのポインターを生成します。|
|[remove_pointer](../standard-library/remove-pointer-class.md)|型へのポインターから型を生成します。|

その他の変換

|||
|-|-|
|[aligned_storage](../standard-library/aligned-storage-class.md)|整列された型の初期化されていないメモリを割り当てます。|
|[aligned_union](../standard-library/aligned-union-class.md)|重要なコンストラクターまたはデストラクターを含む整列された共用体の初期化されていないメモリを割り当てます。|
|[common_type](../standard-library/common-type-class.md)|パラメーター パックのすべての型の共通の型を生成します。|
|[conditional](../standard-library/conditional-class.md)|条件が true の場合は、最初に指定された型が生成され、それ以外の場合、2 番目に指定された型になります。|
|[decay](../standard-library/decay-class.md)|値で渡された型を生成します。 非参照、非定数、非揮発の型、または型へのポインターを作成します。|
|[enable_if](../standard-library/enable-if-class.md)|条件が true の場合は、指定された型が生成され、それ以外の場合、型は生成されません。|
|[result_of](../standard-library/result-of-class.md)|指定された引数型を受け取る呼び出し可能型の戻り値の型を決定します。|
|[underlying_type](../standard-library/underlying-type-class.md)|列挙型の基になる整数型を生成します。|

## <a name="see-also"></a>関連項目

[\<functional>](../standard-library/functional.md)<br/>
