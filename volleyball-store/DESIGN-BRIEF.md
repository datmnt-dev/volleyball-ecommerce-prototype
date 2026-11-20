# UI/UX master brief — Dự án bán đồ bóng chuyền (SÂN/06, tên tạm)

## 1) Mục tiêu

Một thương hiệu bán **áo đấu, áo tập, quần, băng gối, vớ, bóng và phụ kiện** cho cộng đồng bóng chuyền Việt Nam. Giai đoạn đầu tạo **hai điểm vào** rõ ràng, không trộn lẫn nhiệm vụ:

- **Landing / Drop 01:** chiến dịch nhận diện thương hiệu và dẫn về bộ sưu tập; cấu trúc kể chuyện, mang dấu ấn thiết kế.
- **Homepage / Store:** trung tâm tìm sản phẩm, khám phá danh mục và bắt đầu luồng mua sắm; tối ưu khả năng dùng trên điện thoại.

Đây là demo; chưa có sản phẩm thật, chính sách hay doanh nghiệp thực. Xác thực toàn bộ trước khi xuất bản.

## 2) Bài toán khách hàng, các giả định để kiểm chứng

Nhóm giả định: sinh viên, người chơi phong trào, các đội/clb địa phương, vận động viên thường xuyên tập luyện (không coi đây là nghiên cứu thị trường đã xác thực). Nhu cầu quan trọng cần kiểm tra qua phỏng vấn: thoải mái vận động, đúng size, chất liệu, phù hợp phong cách, dễ chọn set, giá rõ ràng, đổi trả, hình ảnh thật.

**3 job-to-be-done:**

1. “Tôi cần quần áo để đi tập hoặc thi đấu, nhanh chóng biết có size phù hợp không.”
2. “Tôi muốn phụ kiện bảo hộ hoặc bóng, cần biết loại, size và công năng thực tế.”
3. “Tôi biết đến brand từ chiến dịch/social, muốn khám phá tinh thần thương hiệu rồi xem và mua hàng.”

## 3) Thương hiệu minh họa

**Tên tạm:** SÂN/06. Số 06 gợi 6 người trên sân mỗi đội, không phải đề xuất tên đã được kiểm tra thương hiệu. **Brand line:** “Chạm bóng. Chạm cá tính.” **Brand manifesto:** “Không chỉ là một trận đấu.” **Personality:** chuyên môn, thân thiện, giàu tinh thần đồng đội, bền bỉ, tự tin, hơi bụi sân trường và thể thao thật; tránh luxury giả và các lời hứa hiệu năng chưa kiểm chứng.

**Visual:** màu giấy ngà/sáng để hàng hóa dễ đọc, deep court navy cho CTA, terracotta để nhấn điểm, vàng mờ gợi quả bóng; headline Barlow Condensed đậm; Manrope cho UI. Ưu tiên bố cục bất đối xứng và ảnh chơi bóng thật. Không sử dụng tím gradient, glass cards, nền aurora, pill button rập khuôn, icon vô nghĩa, text tiếng Anh trang trí quá mức.

## 4) Homepage — wireframe content chi tiết

| Section | Nội dung | Mục tiêu | CTA |
|---|---|---|---|
| Utility bar | Thông báo thực, tránh giả freeship/discount | Làm rõ trạng thái | Câu chuyện thương hiệu |
| Header | Logo, danh mục, shop, story, search, cart | Điều hướng dễ nhận biết | Tìm kiếm / Giỏ |
| Hero | Headline, value prop, ảnh bóng chuyền, 2 CTA | Định vị + vào catalog | Khám phá sản phẩm |
| Categories | 4 vùng áo, đồ tập, bảo hộ, phụ kiện | Giảm thời gian tìm hàng | Chọn category |
| Featured products | 7 SKU demo; lọc danh mục, giá, tên, nhãn | Sản phẩm có thể mua | Quick view / chọn size |
| Brand story | Ý nghĩa 06, nghệ thuật mặt sân | Tạo dấu ấn | Đọc brand story |
| Size guidance | Size modal & disclaimers | Hạn chế sai size | Xem bảng size |
| Newsletter demo | Form kiểm tra email | Thử nghiệm hành vi đăng ký | Submit demo |
| Footer | 3 nhóm điều hướng cơ bản, trạng thái demo | Điều hướng phụ | Shop/FAQ/contact |

## 5) Landing page — wireframe content chi tiết

| Section | Nội dung | Mục tiêu |
|---|---|---|
| Campaign hero | Full-screen action shot, big headline, issue number | Gây ấn tượng về brand |
| Manifesto | 3 dòng tuyên ngôn, giải thích SÂN/06 | Đi sâu vào cảm xúc |
| Lookbook | Editorial volleyball photo + áo phác thảo | Liên kết phong cách và sản phẩm |
| Drop 01 | 3 sản phẩm concept, quick view | Tăng chuyển sang khám phá shop |
| Team statement | Quote về đồng đội — câu slogan sáng tác, không phải review | Tăng cảm giác cộng đồng |
| FAQ | Demo/size/công năng | Minh bạch, giải tỏa câu hỏi |
| CTA cuối | Vào cửa hàng | Chuyển đổi sang sản phẩm |

## 6) Interaction spec

- Tab focus rõ; button là button, link là link; `dialog` cho tìm kiếm, quick view, cart, bảng size.
- Quick view phải lựa chọn kích thước trước khi thêm. Giỏ lưu theo product+variant; thay số lượng/xóa; subtotal tính tức thời; không có “checkout” giả.
- Bộ lọc cập nhật số lượng; search trả kết quả tương ứng tên/category/màu; trình bày empty-state rõ ràng.
- Newsletter được ghi rõ chưa gửi, không thu thập email.
- Trên điện thoại menu hamburger, category 2 cột, card sản phẩm 2 cột, CTA tương đối lớn. Tắt motion cho `prefers-reduced-motion`.

## 7) Motion direction — kế thừa vừa phải từ datmnt-dev

Từ những bằng chứng dự án trước: portfolio có spotlight/3D motion, TripMate cinematic hero và editorial reveal; mobile có token typography. Chỉ nên mượn **ngôn ngữ cảm giác**: một động tác entrance hero, tương tác product hover rất nhẹ, marquee chạy chậm khi người dùng cho phép. Không “animate everything”. Mobile ưu tiên ổn định hơn trưng diễn.

## 8) Template research shortlist (source of inspiration, not licensed assets)

| Reference | Link | Nên học | Không nên sao chép |
|---|---|---|---|
| Shopify Impact | https://themes.shopify.com/themes/impact/presets/impact | Shop nhiều danh mục, merchandising thể thao, visual bold | Màu sắc/hero mặc định |
| Shopify Prestige | https://themes.shopify.com/themes/prestige/presets/prestige | Editorial story, ảnh sản phẩm và lookbook | Xử lý luxury quá mức so với thị trường |
| Shopify Horizon | https://themes.shopify.com/themes/horizon/presets/horizon | Tổ chức hàng hóa, nền tảng store gọn, dễ thử nhanh | Kiểu default mass-market |
| Vercel Commerce | https://examples.vercel.com/templates/template/nextjs-commerce | Kiến trúc storefront thật: product, cart, commerce integration | Visual theme mặc định |
| LOVB Shop | https://shop.lovb.com/ | Ngôn ngữ hình ảnh volleyball, athlete lifestyle | Hình ảnh/brand asset không thuộc sở hữu |
| Volleyballa | https://volleyballa.com/ | Cách nhóm phụ kiện, giải pháp cho fan bóng chuyền | Copy nội dung sản phẩm/branding |

**Recommendation:** nếu bán nhanh và team nhỏ, Shopify Horizon/Impact làm base rồi tùy biến sâu. Nếu đây còn là dự án portfolio kỹ thuật và ưu tiên design-engineering, Next.js Commerce hoặc Shopify headless làm nền kiến trúc, giữ visual riêng từ prototype.

## 9) Anthropic frontend-design skill — cách áp dụng

Nguồn chính thức: https://github.com/anthropics/claude-code/blob/main/plugins/frontend-design/skills/frontend-design/SKILL.md

Mấu chốt: xác định mục tiêu, giọng điệu thị giác, typography, color, composition, motion và **một điểm dễ nhớ** trước khi code; tự đối chiếu những pattern AI UI quen thuộc; tránh thiết kế “đẹp nhưng vô danh”; đảm bảo code vận hành.

Một cách thêm skill từ public catalog vào Claude Code (tham khảo documentation được công bố):

```bash
npx skills add https://github.com/anthropics/claude-code --skill frontend-design
```

Không nhầm với việc ChatGPT đã cài skill này: trong phiên này nội dung định hướng được tổng hợp từ trang công khai của Anthropic, chứ không claim skill đã chạy trong Claude Code của bạn.

### Copyable implementation brief (dùng cho agent/frontend designer)

> Build a two-entry-point Vietnamese volleyball apparel e-commerce experience: (1) a brand campaign landing page at `/drop-01` designed for paid/social traffic, and (2) a commercial homepage at `/` for product discovery. Treat SÂN/06 as a fictional placeholder name until branding approval. Use the provided site files, design brief, and all product SVG assets as the current prototype source of truth. Apply Anthropic frontend-design principles explicitly: set a distinct and domain-specific visual direction, challenge common AI-generated layout patterns, choose intentional typography and motion, prioritize usable interaction over decoration, and ensure responsive accessible code. Preserve the brand's court-navy / warm-paper / rust / volleyball-gold tokens and Vietnamese copy. Rebuild with Next.js App Router, TypeScript and reusable components; isolate product data from UI, then connect only to approved commerce services. Do not add fake testimonials, promotions, unverifiable textile claims, or a fake checkout. Provide desktop/mobile screenshots, documented design decisions, keyboard and functional tests, and outstanding production dependencies. Preserve previous UI/UX personality from the datmnt-dev portfolio/TripMate (editorial rhythm + restrained cinematic hero) without excessive 3D and page-wide animations.

## 10) Information architecture when expanding the site

```
/
/drop-01
/collections
/collections/[category]
/products/[handle]
/search
/cart
/account (optional for initial launch)
/size-guide
/about
/contact
/faq
/shipping-policy
/returns-policy
/privacy-policy
/terms
```

## 11) Priority implementation schedule (not a commitment)

- **P0:** validate target customer, brand assets/name, exact SKUs/variants/photos, shipping and returns economics; review IA and design tokens.
- **P1:** rebuild two prototype pages in production stack; test visually at 375/768/1440px; commit component library.
- **P2:** collection/PDP/cart/checkout integration with verified inventory and server-side pricing, email capture only with explicit consent and actual backend.
- **P3:** content, legal pages, SEO/search, real analytics, product photo performance and accessibility, QA before launch.

**Success measures to track after launch:** add-to-cart rate, PDP→cart rate, checkout completion, mobile search/filter task success, size/returns feedback, Core Web Vitals. No fabricated baseline or targets.
