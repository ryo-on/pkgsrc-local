# $NetBSD$
#

DISTNAME=	Yanone-Kaffeesatz
PKGNAME=	yanone-kaffeesatz-1
CATEGORIES=	fonts
MASTER_SITES=	http://ryo-on.users.sourceforge.net/distrib/fonts/
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://www.fontsquirrel.com/fonts/Yanone-Kaffeesatz
COMMENT=	Yanone Kaffeesatz is sans-serif font family
LICENSE=	open-font-license

PKG_DESTDIR_SUPPORT=	user-destdir

USE_X11BASE=	yes
NO_CONFIGURE=	yes
NO_BUILD=	yes

DOCSDIR=	${PREFIX}/share/doc/${PKGBASE}

INSTALLATION_DIRS=	lib/X11/fonts/TTF \
			${DOCSDIR}

FONTDIR=	${PREFIX}/lib/X11/fonts/TTF
FONTS_DIRS.ttf=	${FONTDIR}

INSTALL_FONTS=	YanoneKaffeesatz-Thin.otf \
		YanoneKaffeesatz-Light.otf \
		YanoneKaffeesatz-Regular.otf \
		YanoneKaffeesatz-Bold.otf

USE_LANGUAGES=	# none

WRKSRC=	${WRKDIR}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
