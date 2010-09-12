# $NetBSD$
#

DISTNAME=	crimson_text_100831
PKGNAME=	${DISTNAME:S/_/-/g}
CATEGORIES=	fonts
MASTER_SITES=	${MASTER_SITE_SOURCEFORGE:=crimsontext/}
EXTRACT_SUFX=	.zip

MAINTAINER=	ryo_on@yk.rim.or.jp
HOMEPAGE=	http://www.aldusleaf.org/
COMMENT=	Crimson Text is a font family for book production
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

INSTALL_FONTS=	CrimsonText-Roman.otf \
		CrimsonText-Italic.otf \
		CrimsonText-Bold.otf \
		CrimsonText-BoldItalic.otf \
		CrimsonText-Semibold.otf \
		CrimsonText-SemiboldItalic.otf
INSTALL_DOCS=	README

USE_LANGUAGES=	# none

WRKSRC=	${WRKDIR}

do-install:
.for fontfile in ${INSTALL_FONTS}
	${INSTALL_DATA} ${WRKSRC}/${fontfile} ${DESTDIR}${FONTDIR}
.endfor
.for docfile in ${INSTALL_DOCS}
	${INSTALL_DATA} ${WRKSRC}/${docfile} ${DESTDIR}${DOCSDIR}
.endfor

.include "../../mk/bsd.pkg.mk"
