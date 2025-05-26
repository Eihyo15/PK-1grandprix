"use client"

import { Button } from "@/components/ui/button"
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card"
import { Badge } from "@/components/ui/badge"
import { Accordion, AccordionContent, AccordionItem, AccordionTrigger } from "@/components/ui/accordion"
import {
  Trophy,
  Calendar,
  MapPin,
  Users,
  Target,
  Clock,
  Award,
  Star,
  CheckCircle,
  Navigation,
  Shield,
  AlertTriangle,
} from "lucide-react"
import Image from "next/image"
import Link from "next/link"

export default function PK1GrandPrixLP() {
  return (
    <div className="min-h-screen bg-white">
      {/* Prize Banner */}
      <div className="bg-gradient-to-r from-yellow-400 to-yellow-600 text-black py-3 text-center font-bold text-lg animate-pulse">
        🏆 優勝賞金20万円！現役大学生限定PK戦トーナメント開催！ 🏆
      </div>

      {/* Header & Hero Section */}
      <section className="relative min-h-screen bg-gradient-to-br from-slate-900 via-blue-900 to-black overflow-hidden">
        {/* Background Pattern */}
        <div className="absolute inset-0 opacity-10">
          <div className="absolute top-20 left-10 w-32 h-32 border border-yellow-400/30 rounded-full"></div>
          <div className="absolute top-40 right-20 w-24 h-24 border border-yellow-400/30 rounded-full"></div>
          <div className="absolute bottom-32 left-1/4 w-16 h-16 border border-yellow-400/30 rounded-full"></div>
          <div className="absolute bottom-20 right-1/3 w-20 h-20 border border-yellow-400/30 rounded-full"></div>
        </div>

        {/* Header */}
        <header className="relative z-10 px-4 lg:px-6 h-16 flex items-center justify-between">
          <div className="flex items-center space-x-2">
            <Target className="h-8 w-8 text-yellow-400" />
            <span className="text-white font-bold text-xl">PK-1 GRAND PRIX</span>
          </div>
          <nav className="hidden md:flex space-x-6">
            <Link href="#overview" className="text-white/80 hover:text-yellow-400 transition-colors">
              概要
            </Link>
            <Link href="#pricing" className="text-white/80 hover:text-yellow-400 transition-colors">
              参加費
            </Link>
            <Link href="#entry" className="text-white/80 hover:text-yellow-400 transition-colors">
              エントリー
            </Link>
            <Link href="#faq" className="text-white/80 hover:text-yellow-400 transition-colors">
              FAQ
            </Link>
          </nav>
        </header>

        {/* Hero Content */}
        <div className="relative z-10 flex flex-col items-center justify-center min-h-[calc(100vh-4rem)] px-4 text-center">
          {/* Logo */}
          <div className="mb-8 transform hover:scale-105 transition-transform duration-300">
            <Image
              src="/images/pk-logo.png"
              width={400}
              height={400}
              alt="PK-1 Grand Prix Logo"
              className="mx-auto drop-shadow-2xl"
            />
          </div>

          <div className="max-w-4xl mx-auto space-y-6">
            <Badge className="bg-gradient-to-r from-yellow-400 to-yellow-600 text-black font-bold px-8 py-4 text-2xl shadow-2xl animate-pulse">
              🏆 優勝賞金20万円 🏆
            </Badge>

            <h1 className="text-4xl md:text-6xl lg:text-7xl font-bold text-white leading-tight">
              <span className="bg-gradient-to-r from-yellow-400 to-yellow-600 bg-clip-text text-transparent">PK-1</span>
              <br />
              GRAND PRIX
              <br />
              <span className="text-3xl md:text-4xl lg:text-5xl">2025</span>
            </h1>

            <p className="text-xl md:text-2xl text-white/90 max-w-3xl mx-auto leading-relaxed">
              現役大学生限定のプレミアムPK戦トーナメント
              <br />
              J-GREEN堺で真の王者を決定せよ
            </p>

            <div className="flex flex-col sm:flex-row gap-4 justify-center items-center mt-8">
              <Link
                href="https://docs.google.com/forms/d/e/1FAIpQLSdg8dwNMRSRKL-0TB12Y11fOUmhfR9I7rjNhXyqd3GAHV9XJg/viewform?usp=header"
                target="_blank"
              >
                <Button
                  size="lg"
                  className="bg-gradient-to-r from-yellow-400 to-yellow-600 hover:from-yellow-500 hover:to-yellow-700 text-black font-bold px-10 py-6 text-xl rounded-full shadow-2xl transform hover:scale-105 transition-all"
                >
                  今すぐエントリー
                </Button>
              </Link>
              <Button
                variant="outline"
                size="lg"
                className="border-2 border-yellow-400 text-yellow-400 hover:bg-yellow-400 hover:text-black px-10 py-6 text-xl rounded-full"
                onClick={() => document.getElementById("details")?.scrollIntoView({ behavior: "smooth" })}
              >
                詳細を見る
              </Button>
            </div>
          </div>

          {/* Scroll Indicator */}
          <div className="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
            <div className="w-6 h-10 border-2 border-yellow-400/50 rounded-full flex justify-center">
              <div className="w-1 h-3 bg-yellow-400/50 rounded-full mt-2"></div>
            </div>
          </div>
        </div>
      </section>

      {/* Event Overview Section */}
      <section id="overview" className="py-20 bg-gradient-to-b from-gray-50 to-white">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <Badge className="bg-blue-100 text-blue-800 px-4 py-2 text-lg mb-4">イベント概要</Badge>
            <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">大学生PKキングを決める戦い</h2>
            <p className="text-xl text-gray-600 max-w-3xl mx-auto">
              J-GREEN堺で開催される、現役大学生限定のプレミアムPK戦トーナメント。最低30チームが参加し、真の王者を決定します。
            </p>
          </div>

          <div className="grid md:grid-cols-2 lg:grid-cols-4 gap-8 mb-16">
            <Card className="text-center p-6 hover:shadow-xl transition-all border-0 bg-white shadow-lg hover:transform hover:scale-105">
              <CardContent className="p-0">
                <div className="w-16 h-16 bg-gradient-to-br from-blue-100 to-blue-200 rounded-full flex items-center justify-center mx-auto mb-4">
                  <Calendar className="h-8 w-8 text-blue-600" />
                </div>
                <h3 className="font-bold text-lg mb-2">開催日</h3>
                <p className="text-2xl font-bold text-blue-600">2025年8月2日</p>
                <p className="text-gray-600">（土曜日）</p>
              </CardContent>
            </Card>

            <Card className="text-center p-6 hover:shadow-xl transition-all border-0 bg-white shadow-lg hover:transform hover:scale-105">
              <CardContent className="p-0">
                <div className="w-16 h-16 bg-gradient-to-br from-green-100 to-green-200 rounded-full flex items-center justify-center mx-auto mb-4">
                  <MapPin className="h-8 w-8 text-green-600" />
                </div>
                <h3 className="font-bold text-lg mb-2">会場</h3>
                <p className="text-2xl font-bold text-green-600">J-GREEN堺</p>
                <p className="text-gray-600">大阪府堺市</p>
              </CardContent>
            </Card>

            <Card className="text-center p-6 hover:shadow-xl transition-all border-0 bg-white shadow-lg hover:transform hover:scale-105">
              <CardContent className="p-0">
                <div className="w-16 h-16 bg-gradient-to-br from-purple-100 to-purple-200 rounded-full flex items-center justify-center mx-auto mb-4">
                  <Users className="h-8 w-8 text-purple-600" />
                </div>
                <h3 className="font-bold text-lg mb-2">募集チーム</h3>
                <p className="text-2xl font-bold text-purple-600">最低30チーム</p>
                <p className="text-gray-600">現役大学生のみ</p>
              </CardContent>
            </Card>

            <Card className="text-center p-6 hover:shadow-xl transition-all border-0 bg-white shadow-lg hover:transform hover:scale-105">
              <CardContent className="p-0">
                <div className="w-16 h-16 bg-gradient-to-br from-yellow-100 to-yellow-200 rounded-full flex items-center justify-center mx-auto mb-4">
                  <Trophy className="h-8 w-8 text-yellow-600" />
                </div>
                <h3 className="font-bold text-lg mb-2">優勝賞金</h3>
                <p className="text-2xl font-bold text-yellow-600">20万円</p>
                <p className="text-gray-600">トーナメントPK戦</p>
              </CardContent>
            </Card>
          </div>

          {/* Tournament Format */}
          <div className="bg-gradient-to-r from-blue-600 to-slate-800 rounded-3xl p-8 md:p-12 text-white">
            <div className="grid md:grid-cols-2 gap-8 items-center">
              <div>
                <h3 className="text-3xl font-bold mb-6">トーナメント形式</h3>
                <div className="space-y-4">
                  <div className="flex items-center space-x-3">
                    <Target className="h-6 w-6 text-yellow-400" />
                    <span className="text-lg">PK戦による勝負</span>
                  </div>
                  <div className="flex items-center space-x-3">
                    <Clock className="h-6 w-6 text-yellow-400" />
                    <span className="text-lg">スピーディーな進行</span>
                  </div>
                  <div className="flex items-center space-x-3">
                    <Award className="h-6 w-6 text-yellow-400" />
                    <span className="text-lg">実力が試される真剣勝負</span>
                  </div>
                  <div className="flex items-center space-x-3">
                    <Star className="h-6 w-6 text-yellow-400" />
                    <span className="text-lg">大学生限定の特別大会</span>
                  </div>
                </div>
              </div>
              <div className="text-center">
                <div className="bg-gradient-to-br from-yellow-400/20 to-yellow-600/20 backdrop-blur-sm rounded-3xl p-10 border-2 border-yellow-400">
                  <Trophy className="h-32 w-32 text-yellow-400 mx-auto mb-6" />
                  <p className="text-3xl font-bold mb-2">🏆 優勝チーム 🏆</p>
                  <p className="text-6xl font-bold text-yellow-400 mb-2">20万円</p>
                  <p className="text-2xl font-bold">獲得！</p>
                  <div className="mt-4 px-6 py-2 bg-yellow-400 text-black rounded-full font-bold text-lg">現金支給</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      {/* Detailed Information Section */}
      <section id="details" className="py-20 bg-gradient-to-br from-slate-50 to-blue-50">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <Badge className="bg-slate-200 text-slate-800 px-4 py-2 text-lg mb-4">大会詳細</Badge>
            <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">詳細情報</h2>
            <p className="text-xl text-gray-600 max-w-3xl mx-auto">
              PK-1グランプリの詳細なルールと試合形式をご確認ください
            </p>
          </div>

          <div className="max-w-6xl mx-auto space-y-8">
            {/* 報酬セクション */}
            <Card className="shadow-xl border-0 overflow-hidden">
              <CardHeader className="bg-gradient-to-r from-yellow-500 to-yellow-600 text-white">
                <CardTitle className="text-2xl font-bold flex items-center">
                  <Trophy className="h-8 w-8 mr-3" />
                  報酬
                </CardTitle>
              </CardHeader>
              <CardContent className="p-8">
                <div className="space-y-4">
                  <div className="flex items-start space-x-3">
                    <div className="w-2 h-2 bg-yellow-500 rounded-full mt-3"></div>
                    <p className="text-lg text-gray-700">
                      決勝トーナメント戦を勝ち抜き優勝した１チームに報酬として
                      <span className="font-bold text-yellow-600 text-xl">20万円</span>を進呈します。
                    </p>
                  </div>
                  <div className="flex items-start space-x-3">
                    <div className="w-2 h-2 bg-yellow-500 rounded-full mt-3"></div>
                    <p className="text-lg text-gray-700">
                      参加チーム数が20チーム未満の場合の優勝報酬は
                      <span className="font-bold text-blue-600">参加チーム数×5,000円</span>とします。
                    </p>
                  </div>
                </div>
              </CardContent>
            </Card>

            {/* 試合形式セクション */}
            <Card className="shadow-xl border-0 overflow-hidden">
              <CardHeader className="bg-gradient-to-r from-blue-500 to-blue-600 text-white">
                <CardTitle className="text-2xl font-bold flex items-center">
                  <Target className="h-8 w-8 mr-3" />
                  試合形式
                </CardTitle>
              </CardHeader>
              <CardContent className="p-8">
                <div className="grid md:grid-cols-2 gap-8">
                  <div className="space-y-4">
                    <div className="flex items-start space-x-3">
                      <div className="w-2 h-2 bg-blue-500 rounded-full mt-3"></div>
                      <p className="text-lg text-gray-700">
                        <span className="font-bold">５人対５人のPK戦</span>をトーナメント方式で行います。
                      </p>
                    </div>
                    <div className="flex items-start space-x-3">
                      <div className="w-2 h-2 bg-blue-500 rounded-full mt-3"></div>
                      <p className="text-lg text-gray-700">
                        <span className="font-bold">GKもキッカー</span>をつとめます。
                      </p>
                    </div>
                    <div className="flex items-start space-x-3">
                      <div className="w-2 h-2 bg-blue-500 rounded-full mt-3"></div>
                      <p className="text-lg text-gray-700">
                        ゴールは<span className="font-bold">フットサルゴールを2個</span>使用。
                      </p>
                    </div>
                  </div>
                  <div className="space-y-4">
                    <div className="flex items-start space-x-3">
                      <div className="w-2 h-2 bg-blue-500 rounded-full mt-3"></div>
                      <p className="text-lg text-gray-700">
                        ボールは<span className="font-bold">サッカーボール5号球</span>を使用。
                      </p>
                    </div>
                    <div className="flex items-start space-x-3">
                      <div className="w-2 h-2 bg-blue-500 rounded-full mt-3"></div>
                      <p className="text-lg text-gray-700">
                        <span className="font-bold">勝敗が決まった時点</span>で試合終了となります。
                      </p>
                    </div>
                    <div className="flex items-start space-x-3">
                      <div className="w-2 h-2 bg-blue-500 rounded-full mt-3"></div>
                      <p className="text-lg text-gray-700">
                        <span className="font-bold text-red-600">１試合目のみ</span>
                        勝敗が決まっても５名全員蹴っていただきます。
                      </p>
                    </div>
                  </div>
                </div>
              </CardContent>
            </Card>

            {/* ルールセクション */}
            <Card className="shadow-xl border-0 overflow-hidden">
              <CardHeader className="bg-gradient-to-r from-green-500 to-green-600 text-white">
                <CardTitle className="text-2xl font-bold flex items-center">
                  <Shield className="h-8 w-8 mr-3" />
                  ルール
                </CardTitle>
              </CardHeader>
              <CardContent className="p-8">
                <div className="grid md:grid-cols-2 gap-8">
                  <div className="space-y-4">
                    <h4 className="font-bold text-lg text-gray-900 mb-3">基本ルール</h4>
                    <div className="space-y-3">
                      <div className="flex items-start space-x-3">
                        <CheckCircle className="h-5 w-5 text-green-500 mt-1" />
                        <p className="text-gray-700">１回戦目は、勝敗が決していても５名全員が蹴る</p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <Clock className="h-5 w-5 text-blue-500 mt-1" />
                        <p className="text-gray-700">
                          審判の合図から<span className="font-bold">10秒以内</span>に蹴らなければPK失敗
                        </p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <Users className="h-5 w-5 text-purple-500 mt-1" />
                        <p className="text-gray-700">ゴールキーパーもキッカーと同じ待機場所で待機</p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <Target className="h-5 w-5 text-orange-500 mt-1" />
                        <p className="text-gray-700">ボールはペナルティーマーク上で静止していなければならない</p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <Star className="h-5 w-5 text-yellow-500 mt-1" />
                        <p className="text-gray-700">キッカーは特定されなければならない</p>
                      </div>
                    </div>
                  </div>

                  <div className="space-y-4">
                    <h4 className="font-bold text-lg text-gray-900 mb-3">反則・その他</h4>
                    <div className="space-y-3">
                      <div className="flex items-start space-x-3">
                        <Shield className="h-5 w-5 text-green-500 mt-1" />
                        <p className="text-gray-700">
                          ゴールキーパーはキッカーが蹴るまで片足がゴールラインを踏んでいなければならない
                        </p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <AlertTriangle className="h-5 w-5 text-red-500 mt-1" />
                        <p className="text-gray-700">キッカーは２回以上ボールに触れてはいけない</p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <AlertTriangle className="h-5 w-5 text-red-500 mt-1" />
                        <p className="text-gray-700">キッカーに反則があった場合はPK失敗とする</p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <CheckCircle className="h-5 w-5 text-blue-500 mt-1" />
                        <p className="text-gray-700">
                          ゴールキーパーに反則があった場合は、ゴール時はゴール、外れた場合は蹴り直し
                        </p>
                      </div>
                      <div className="flex items-start space-x-3">
                        <Clock className="h-5 w-5 text-purple-500 mt-1" />
                        <p className="text-gray-700">延長戦も順番通りに蹴らなければならない</p>
                      </div>
                    </div>
                  </div>
                </div>

                <div className="mt-8 p-6 bg-red-50 border-2 border-red-200 rounded-lg">
                  <div className="flex items-center space-x-2 mb-2">
                    <AlertTriangle className="h-6 w-6 text-red-600" />
                    <h4 className="font-bold text-lg text-red-800">重要な注意事項</h4>
                  </div>
                  <p className="text-red-700">
                    予定時刻が早まるなどにより試合時間が変更になった場合でも、その時に
                    <span className="font-bold">３名揃っていないチームは失格（不戦敗）</span>となります。
                  </p>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Pricing Section */}
      <section id="pricing" className="py-20 bg-gradient-to-br from-yellow-50 via-yellow-100 to-yellow-200">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <Badge className="bg-yellow-600 text-white px-4 py-2 text-lg mb-4">参加費・エントリープラン</Badge>
            <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">お得なプランをご用意</h2>
            <p className="text-xl text-gray-700 max-w-3xl mx-auto">
              早割や団体割など、様々なプランで参加しやすい料金設定
            </p>
          </div>

          <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
            {/* 早割プラン */}
            <Card className="relative overflow-hidden border-2 border-yellow-300 shadow-xl hover:shadow-2xl transition-all hover:transform hover:scale-105">
              <div className="absolute top-0 right-0 bg-red-500 text-white px-4 py-1 text-sm font-bold">人気No.1</div>
              <CardHeader className="text-center pb-4">
                <CardTitle className="text-2xl font-bold text-gray-900">早割プラン</CardTitle>
                <div className="text-4xl font-bold text-yellow-600">¥10,000</div>
                <p className="text-gray-600">/チーム</p>
              </CardHeader>
              <CardContent>
                <div className="space-y-3 mb-6">
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>6月30日まで限定</span>
                  </div>
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>5名まで参加可能</span>
                  </div>
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>最もお得な料金</span>
                  </div>
                </div>
                <Link
                  href="https://docs.google.com/forms/d/e/1FAIpQLSdg8dwNMRSRKL-0TB12Y11fOUmhfR9I7rjNhXyqd3GAHV9XJg/viewform?usp=header"
                  target="_blank"
                >
                  <Button className="w-full bg-yellow-600 hover:bg-yellow-700 text-white font-bold py-3">
                    早割で申し込む
                  </Button>
                </Link>
              </CardContent>
            </Card>

            {/* 通常プラン */}
            <Card className="border-2 border-gray-200 shadow-xl hover:shadow-2xl transition-all hover:transform hover:scale-105">
              <CardHeader className="text-center pb-4">
                <CardTitle className="text-2xl font-bold text-gray-900">通常プラン</CardTitle>
                <div className="text-4xl font-bold text-blue-600">¥15,000</div>
                <p className="text-gray-600">/チーム</p>
              </CardHeader>
              <CardContent>
                <div className="space-y-3 mb-6">
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>7月1日〜7月27日</span>
                  </div>
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>5名まで参加可能</span>
                  </div>
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>標準料金</span>
                  </div>
                </div>
                <Link
                  href="https://docs.google.com/forms/d/e/1FAIpQLSdg8dwNMRSRKL-0TB12Y11fOUmhfR9I7rjNhXyqd3GAHV9XJg/viewform?usp=header"
                  target="_blank"
                >
                  <Button
                    variant="outline"
                    className="w-full border-blue-600 text-blue-600 hover:bg-blue-600 hover:text-white font-bold py-3"
                  >
                    通常プランで申し込む
                  </Button>
                </Link>
              </CardContent>
            </Card>

            {/* 団体割プラン */}
            <Card className="border-2 border-purple-300 shadow-xl hover:shadow-2xl transition-all hover:transform hover:scale-105">
              <CardHeader className="text-center pb-4">
                <CardTitle className="text-2xl font-bold text-gray-900">団体割プラン</CardTitle>
                <div className="text-4xl font-bold text-purple-600">¥10,000</div>
                <p className="text-gray-600">/チーム</p>
              </CardHeader>
              <CardContent>
                <div className="space-y-3 mb-6">
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>2チーム以上同時エントリー</span>
                  </div>
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>5名まで参加可能</span>
                  </div>
                  <div className="flex items-center space-x-2">
                    <CheckCircle className="h-5 w-5 text-green-500" />
                    <span>複数チームでお得</span>
                  </div>
                </div>
                <Link
                  href="https://docs.google.com/forms/d/e/1FAIpQLSdg8dwNMRSRKL-0TB12Y11fOUmhfR9I7rjNhXyqd3GAHV9XJg/viewform?usp=header"
                  target="_blank"
                >
                  <Button
                    variant="outline"
                    className="w-full border-purple-600 text-purple-600 hover:bg-purple-600 hover:text-white font-bold py-3"
                  >
                    団体割で申し込む
                  </Button>
                </Link>
              </CardContent>
            </Card>
          </div>

          {/* 追加オプション */}
          <div className="mt-12 grid md:grid-cols-2 gap-8 max-w-4xl mx-auto">
            <Card className="border-2 border-orange-300 shadow-lg">
              <CardHeader className="text-center">
                <CardTitle className="text-xl font-bold text-orange-600">個人参加</CardTitle>
              </CardHeader>
              <CardContent className="text-center">
                <div className="text-3xl font-bold text-orange-600 mb-2">¥3,000</div>
                <p className="text-gray-600 mb-4">/人（運営でチーム編成）</p>
                <Link
                  href="https://docs.google.com/forms/d/e/1FAIpQLSdg8dwNMRSRKL-0TB12Y11fOUmhfR9I7rjNhXyqd3GAHV9XJg/viewform?usp=header"
                  target="_blank"
                >
                  <Button
                    variant="outline"
                    className="border-orange-600 text-orange-600 hover:bg-orange-600 hover:text-white"
                  >
                    個人参加で申し込む
                  </Button>
                </Link>
              </CardContent>
            </Card>

            <Card className="border-2 border-green-300 shadow-lg">
              <CardHeader className="text-center">
                <CardTitle className="text-xl font-bold text-green-600">追加メンバー</CardTitle>
              </CardHeader>
              <CardContent className="text-center">
                <div className="text-3xl font-bold text-green-600 mb-2">+¥1,000</div>
                <p className="text-gray-600 mb-4">/人（1チーム6名以上の場合）</p>
                <Link
                  href="https://docs.google.com/forms/d/e/1FAIpQLSdg8dwNMRSRKL-0TB12Y11fOUmhfR9I7rjNhXyqd3GAHV9XJg/viewform?usp=header"
                  target="_blank"
                >
                  <Button
                    variant="outline"
                    className="border-green-600 text-green-600 hover:bg-green-600 hover:text-white"
                  >
                    追加メンバー登録
                  </Button>
                </Link>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Entry Method Section */}
      <section id="entry" className="py-20 bg-white">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <Badge className="bg-blue-100 text-blue-800 px-4 py-2 text-lg mb-4">エントリー方法</Badge>
            <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">簡単2ステップでエントリー</h2>
          </div>

          <div className="max-w-4xl mx-auto">
            <div className="grid md:grid-cols-2 gap-8">
              {/* STEP 1 */}
              <Card className="p-8 shadow-xl border-2 border-blue-200 hover:shadow-2xl transition-all">
                <CardContent className="p-0 text-center">
                  <div className="w-20 h-20 bg-gradient-to-br from-blue-500 to-blue-600 rounded-full flex items-center justify-center mx-auto mb-6">
                    <span className="text-white font-bold text-2xl">1</span>
                  </div>
                  <h3 className="text-2xl font-bold text-gray-900 mb-4">エントリーフォームから申込</h3>
                  <p className="text-gray-600 mb-6">Googleフォームから必要事項を入力してお申し込みください</p>
                  <Link
                    href="https://docs.google.com/forms/d/e/1FAIpQLSdg8dwNMRSRKL-0TB12Y11fOUmhfR9I7rjNhXyqd3GAHV9XJg/viewform?usp=header"
                    target="_blank"
                  >
                    <Button className="bg-gradient-to-r from-blue-500 to-blue-600 hover:from-blue-600 hover:to-blue-700 text-white font-bold px-8 py-3 rounded-full">
                      エントリーはこちら
                    </Button>
                  </Link>
                </CardContent>
              </Card>

              {/* STEP 2 */}
              <Card className="p-8 shadow-xl border-2 border-green-200 hover:shadow-2xl transition-all">
                <CardContent className="p-0 text-center">
                  <div className="w-20 h-20 bg-gradient-to-br from-green-500 to-green-600 rounded-full flex items-center justify-center mx-auto mb-6">
                    <span className="text-white font-bold text-2xl">2</span>
                  </div>
                  <h3 className="text-2xl font-bold text-gray-900 mb-4">公式LINE友だち登録</h3>
                  <p className="text-gray-600 mb-6">
                    <span className="font-bold text-red-600">全員必須！</span>大会情報や連絡事項をお送りします
                  </p>

                  {/* QR Code */}
                  <div className="bg-white p-4 rounded-lg mb-4 mx-auto w-48 h-48 flex items-center justify-center shadow-lg">
                    <Image
                      src="/images/line-qr.png"
                      width={180}
                      height={180}
                      alt="LINE公式アカウント QRコード"
                      className="rounded-lg"
                    />
                  </div>

                  <Link href="https://line.me/R/ti/p/@250mifis?ts=05251159&oat_content=url" target="_blank">
                    <Button className="bg-gradient-to-r from-green-500 to-green-600 hover:from-green-600 hover:to-green-700 text-white font-bold px-8 py-3 rounded-full">
                      公式LINEに登録する
                    </Button>
                  </Link>
                </CardContent>
              </Card>
            </div>

            <div className="mt-12 p-6 bg-yellow-50 border-2 border-yellow-300 rounded-2xl">
              <div className="flex items-center justify-center space-x-2 mb-4">
                <AlertTriangle className="h-6 w-6 text-yellow-600" />
                <h4 className="font-bold text-lg text-yellow-800">重要なお知らせ</h4>
              </div>
              <p className="text-yellow-800 text-center">
                公式LINE登録は参加者全員必須です。登録がない場合、大会に参加できませんのでご注意ください。
              </p>
            </div>
          </div>
        </div>
      </section>

      {/* FAQ Section */}
      <section id="faq" className="py-20 bg-gray-50">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <Badge className="bg-gray-200 text-gray-800 px-4 py-2 text-lg mb-4">よくある質問</Badge>
            <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">FAQ</h2>
          </div>

          <div className="max-w-4xl mx-auto">
            <Accordion type="single" collapsible className="space-y-4">
              <AccordionItem value="item-1" className="bg-white rounded-lg shadow-md border-0">
                <AccordionTrigger className="px-6 py-4 text-left font-semibold text-lg hover:no-underline">
                  1チーム何人まで参加できますか？
                </AccordionTrigger>
                <AccordionContent className="px-6 pb-4 text-gray-600">
                  原則5名までです。6名以上の場合は追加メンバー料金として1名ごとに+1,000円が必要です。
                </AccordionContent>
              </AccordionItem>

              <AccordionItem value="item-2" className="bg-white rounded-lg shadow-md border-0">
                <AccordionTrigger className="px-6 py-4 text-left font-semibold text-lg hover:no-underline">
                  個人参加はできますか？
                </AccordionTrigger>
                <AccordionContent className="px-6 pb-4 text-gray-600">
                  可能です！個人参加の場合は3,000円/人で、運営側でチーム編成を行います。
                </AccordionContent>
              </AccordionItem>

              <AccordionItem value="item-3" className="bg-white rounded-lg shadow-md border-0">
                <AccordionTrigger className="px-6 py-4 text-left font-semibold text-lg hover:no-underline">
                  スパイクは使用できますか？
                </AccordionTrigger>
                <AccordionContent className="px-6 pb-4 text-gray-600">
                  J-GREEN堺のルールに準拠します。人工芝用スパイクまたはトレーニングシューズをご使用ください。
                </AccordionContent>
              </AccordionItem>

              <AccordionItem value="item-4" className="bg-white rounded-lg shadow-md border-0">
                <AccordionTrigger className="px-6 py-4 text-left font-semibold text-lg hover:no-underline">
                  キャンセル・返金はできますか？
                </AccordionTrigger>
                <AccordionContent className="px-6 pb-4 text-gray-600">
                  原則として返金は行っておりません。やむを得ない事情がある場合は個別にご相談ください。
                </AccordionContent>
              </AccordionItem>

              <AccordionItem value="item-5" className="bg-white rounded-lg shadow-md border-0">
                <AccordionTrigger className="px-6 py-4 text-left font-semibold text-lg hover:no-underline">
                  雨天時はどうなりますか？
                </AccordionTrigger>
                <AccordionContent className="px-6 pb-4 text-gray-600">
                  荒天時は中止・順延の可能性があります。開催可否は前日までに公式LINEでお知らせします。
                </AccordionContent>
              </AccordionItem>
            </Accordion>
          </div>
        </div>
      </section>

      {/* Access Section */}
      <section id="access" className="py-20 bg-white">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <Badge className="bg-green-100 text-green-800 px-4 py-2 text-lg mb-4">アクセス</Badge>
            <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">会場案内</h2>
          </div>

          <div className="max-w-6xl mx-auto">
            <Card className="overflow-hidden shadow-2xl">
              <div className="grid md:grid-cols-2">
                <div className="p-8">
                  <h3 className="text-2xl font-bold text-gray-900 mb-6">J-GREEN堺</h3>
                  <div className="space-y-4">
                    <div className="flex items-start space-x-3">
                      <MapPin className="h-6 w-6 text-green-600 mt-1" />
                      <div>
                        <p className="font-semibold">住所</p>
                        <p className="text-gray-600">大阪府堺市堺区築港八幡町145</p>
                      </div>
                    </div>
                    <div className="flex items-start space-x-3">
                      <Navigation className="h-6 w-6 text-blue-600 mt-1" />
                      <div>
                        <p className="font-semibold">アクセス</p>
                        <p className="text-gray-600">南海本線「堺駅」からバス約10分</p>
                        <p className="text-gray-600">阪神高速「堺IC」から車約5分</p>
                      </div>
                    </div>
                    <div className="flex items-start space-x-3">
                      <Clock className="h-6 w-6 text-purple-600 mt-1" />
                      <div>
                        <p className="font-semibold">駐車場</p>
                        <p className="text-gray-600">有料駐車場あり（約1,000台）</p>
                      </div>
                    </div>
                  </div>
                </div>
                <div className="bg-gray-100 p-8 flex items-center justify-center">
                  <div className="text-center text-gray-500">
                    <MapPin className="h-24 w-24 mx-auto mb-4" />
                    <p className="text-lg">地図・詳細案内</p>
                    <p className="text-sm">J-GREEN堺公式サイトをご確認ください</p>
                  </div>
                </div>
              </div>
            </Card>
          </div>
        </div>
      </section>

      {/* Terms Section */}
      <section className="py-20 bg-gray-50">
        <div className="container mx-auto px-4">
          <div className="text-center mb-16">
            <Badge className="bg-gray-200 text-gray-800 px-4 py-2 text-lg mb-4">注意事項・規約</Badge>
            <h2 className="text-4xl md:text-5xl font-bold text-gray-900 mb-6">大会規約</h2>
          </div>

          <div className="max-w-4xl mx-auto">
            <Card className="p-8 shadow-xl">
              <CardContent className="p-0">
                <div className="grid md:grid-cols-2 gap-8">
                  <div>
                    <h3 className="text-xl font-bold text-gray-900 mb-4 flex items-center">
                      <Shield className="h-6 w-6 text-blue-600 mr-2" />
                      参加資格・条件
                    </h3>
                    <ul className="space-y-2 text-gray-600">
                      <li>• 現役大学生のみ参加可能</li>
                      <li>• 学生証の提示が必要</li>
                      <li>• 公式LINE登録必須（全員）</li>
                      <li>• 適切なサッカー用具着用</li>
                      <li>• 健康状態良好な方のみ</li>
                    </ul>
                  </div>
                  <div>
                    <h3 className="text-xl font-bold text-gray-900 mb-4 flex items-center">
                      <Trophy className="h-6 w-6 text-yellow-600 mr-2" />
                      賞金・免責事項
                    </h3>
                    <ul className="space-y-2 text-gray-600">
                      <li>• 優勝賞金は大会終了後支払い</li>
                      <li>• 怪我等の責任は負いかねます</li>
                      <li>• 大会中の写真・動画使用許可</li>
                      <li>• 天候等による中止の場合返金なし</li>
                      <li>• 規約違反時は失格処分</li>
                    </ul>
                  </div>
                </div>

                <div className="mt-8 p-6 bg-red-50 border-2 border-red-200 rounded-lg">
                  <h4 className="font-bold text-lg text-red-800 mb-2 flex items-center">
                    <AlertTriangle className="h-6 w-6 mr-2" />
                    重要事項
                  </h4>
                  <p className="text-red-700">
                    公式LINE登録は参加者全員必須です。未登録の場合は大会参加をお断りする場合があります。
                    また、大会当日は学生証を必ずご持参ください。
                  </p>
                </div>
              </CardContent>
            </Card>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="bg-gradient-to-r from-slate-900 to-blue-900 text-white py-12">
        <div className="container mx-auto px-4">
          <div className="text-center">
            <div className="flex items-center justify-center space-x-3 mb-6">
              <Image
                src="/images/pk-logo.png"
                width={60}
                height={60}
                alt="PK-1 Grand Prix Logo"
                className="drop-shadow-lg"
              />
              <div>
                <h3 className="font-bold text-2xl">PK-1 GRAND PRIX 2025</h3>
                <p className="text-yellow-400">大学生限定プレミアムPK戦トーナメント</p>
              </div>
            </div>

            <div className="mb-6">
              <p className="text-lg font-semibold text-yellow-400">主催</p>
              <p className="text-xl font-bold">PK-1グランプリ実行委員会</p>
            </div>

            <div className="flex justify-center space-x-8 text-sm text-gray-300 mb-6">
              <Link href="#" className="hover:text-yellow-400 transition-colors">
                プライバシーポリシー
              </Link>
              <Link href="#" className="hover:text-yellow-400 transition-colors">
                利用規約
              </Link>
              <Link href="#" className="hover:text-yellow-400 transition-colors">
                お問い合わせ
              </Link>
            </div>

            <div className="border-t border-gray-600 pt-6">
              <p className="text-gray-400 text-sm">© 2025 PK-1 Grand Prix Executive Committee. All rights reserved.</p>
            </div>
          </div>
        </div>
      </footer>
    </div>
  )
}
